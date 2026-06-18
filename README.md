# TS Nails — записи на маникюр

Приложение для учёта клиентов и записей. Данные хранятся в **Firebase Firestore**, вход — через **Google**.

Репозиторий: [github.com/iga0077/TS-NAILS](https://github.com/iga0077/TS-NAILS)

## Как устроен доступ

1. Пользователь входит через Google.
2. Firebase проверяет, есть ли его Gmail в коллекции **`allowedUsers`**.
3. Если да — он видит **только свои** записи и клиентов (по своему Firebase UID).
4. Если нет — показывается экран «Нет доступа».

У каждого человека **отдельная база**: мама видит только своих клиентов, другой аккаунт — только своих.

## Первоначальная настройка Firebase

### 1. Authentication

В [Firebase Console](https://console.firebase.google.com/project/ts-nails/authentication/providers):

- Включите **Google** как способ входа.
- В **Authorized domains** добавьте домен, где будет сайт (например `ts-nails.web.app`).

### 2. Firestore

Создайте базу Firestore (режим **production**).

### 3. Правила безопасности

```bash
firebase deploy --only firestore:rules
```

Или вставьте содержимое `firestore.rules` в Firebase Console → Firestore → Rules.

### 4. Добавить разрешённые Gmail

Firebase Console → **Firestore** → **Start collection**:

| Поле | Значение |
|------|----------|
| Collection ID | `allowedUsers` |
| Document ID | **полный Gmail**, например `mama@gmail.com` |
| Field | `active` (boolean) = `true` |
| Field | `name` (string) = имя, например `Мама` |

Повторите для каждого человека. **Document ID = Gmail целиком.**

Пример:

```
allowedUsers/
  mama@gmail.com/     { active: true, name: "Мама" }

users/
  {uid}/
    records/{id}
    clients/{id}
```

Чтобы отключить доступ — удалите документ или поставьте `active: false`.

### 5. Публикация

```bash
npm install -g firebase-tools
firebase login
firebase deploy --only hosting,firestore:rules
```

## Локальный запуск

```bash
npx serve .
```

Google Auth не работает через `file://` — нужен локальный сервер.

## Миграция с localStorage

При первом входе старые данные из браузера автоматически переносятся в Firestore, если облако пустое.
