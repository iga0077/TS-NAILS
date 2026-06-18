# TS Nails — записи на маникюр

Приложение для учёта клиентов и записей. Данные в **Firebase Firestore**, вход через **Google**.

- Репозиторий: [github.com/iga0077/TS-NAILS](https://github.com/iga0077/TS-NAILS)
- Сайт (GitHub Pages): **https://iga0077.github.io/TS-NAILS/**

## Как устроен доступ

1. Вход через Google.
2. Firebase проверяет Gmail в коллекции **`allowedUsers`**.
3. Если есть — пользователь видит **только свои** записи и клиентов.
4. Если нет — экран «Нет доступа».

У каждого человека **отдельная база** (по Firebase UID): каждый видит только своих клиентов.

## Безопасность и ключи Firebase

**Ключи в `index.html` на GitHub — это нормально.** У Firebase для веб-приложений конфиг (`apiKey`, `projectId` и т.д.) всегда публичный: он в коде страницы у каждого пользователя. Это не пароль и не даёт доступ к чужим данным.

Защита строится на другом:

| Уровень | Что делает |
|--------|------------|
| **Google Auth** | Войти может только с Google-аккаунтом |
| **`allowedUsers`** | Даже после входа доступ только у Gmail из белого списка |
| **`firestore.rules`** | Каждый читает/пишет только `users/{свой uid}/...` |
| **Authorized domains** | Google-вход работает только с вашего домена Pages |

`Firebase.txt` в репозиторий не попадает (`.gitignore`), но тот же конфиг есть в `index.html` — так и задумано для фронтенда.

**Не публикуйте** только серверные секреты (Service Account JSON, private keys) — их в проекте нет.

Опционально позже: [Firebase App Check](https://firebase.google.com/docs/app-check) — защита от злоупотребления публичным `apiKey`.

## Настройка Firebase

### 1. Authentication

[Firebase Console → Authentication](https://console.firebase.google.com/project/ts-nails/authentication/providers):

- Включите **Google**.
- В **Authorized domains** добавьте: **`iga0077.github.io`**

### 2. Firestore

Создайте базу (режим production).

### 3. Правила

```bash
firebase deploy --only firestore:rules
```

Или вставьте `firestore.rules` в Console → Firestore → Rules.

### 4. Разрешённые Gmail

Firestore → коллекция **`allowedUsers`**:

| | |
|---|---|
| Document ID | полный Gmail, например `mama@gmail.com` |
| `active` | `true` |
| `name` | имя (необязательно) |

Пример:

```
allowedUsers/
  user@gmail.com/     { active: true, name: "user" }

users/
  {uid}/
    records/{id}
    clients/{id}
```

## Публикация на GitHub Pages

Сайт деплоится автоматически при push в `main` (workflow `.github/workflows/pages.yml`).

Первый раз в GitHub: **Settings → Pages → Build and deployment → GitHub Actions**.

Firebase Hosting не используется (бесплатный тариф есть, но сейчас не нужен).

## Локальный запуск

```bash
npx serve .
```

Google Auth не работает через `file://`.

## PWA (установка на телефон)

Приложение можно добавить на главный экран:

- **Android (Chrome):** меню → «Установить приложение» / «Добавить на главный экран»
- **iPhone (Safari):** «Поделиться» → «На экран Домой»

Работает оболочка приложения офлайн; для входа и синхронизации записей нужен интернет.

## Миграция с localStorage

При первом входе старые данные из браузера переносятся в Firestore, если облако пустое.
