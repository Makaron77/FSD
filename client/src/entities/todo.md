//! архитектура entities - бизнес-сущности, с которыми работает проект, например user или product(Не обязательный слой).

// ? Его стоит добавлять только в случае сложного или крупного приложения, где важно разделить бизнес-логику и интерфейсы ключевых сущностей.
// ? В малых и средних проектах ты можешь обойтись без него, распределив логику по другим слоям.
// src/
// ├── entities/
// │   └── user/
// │       ├── model/            # Слайсы, селекторы, асинхронные thunks
// │       │   ├── slice.ts
// │       │   ├── selectors.ts
// │       │   └── thunks.ts     # Если используете thunks отдельно
// │       ├── api/              # Функции для запросов
// │       │   └── userApi.ts    # HTTP-запросы, например, через axios
// │       ├── ui/               # Компоненты и модули интерфейса
// │       │   ├── UserProfile/
// │       │   │   ├── index.tsx
// │       │   │   ├── UserProfile.module.css
// │       │   │   └── types.ts  # Локальные типы, если нужны
// │       │   └── ...
// │       ├── lib/              # Вспомогательные функции и утилиты
// │       └── index.ts          # используется для объединения всех экспортов этого модуля в одном месте. 