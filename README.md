# TS Nails

Записи клиентов на маникюр. Сайт: **https://iga0077.github.io/TS-NAILS/**

Вход через Google. Данные в Firebase — у каждого пользователя своя база.

## Доступ

Gmail должен быть в Firestore → коллекция `allowedUsers` (Document ID = email, поле `active: true`).

## Firebase

- [Authentication](https://console.firebase.google.com/project/ts-nails/authentication/providers): Google, домен `iga0077.github.io`
- Правила: `firestore.rules` → `firebase deploy --only firestore:rules`

## PWA

На телефоне: Chrome → «Установить приложение» или Safari → «На экран Домой».
