src/
├── pages/
│   └── HomePage/                 # Пример страницы
│       ├── index.tsx             # Входная точка страницы
│       ├── HomePage.module.css   # Стили страницы
│       ├── ui/                   # Компоненты, используемые только на этой странице
│       │   ├── HeaderSection/      # Компонент, используемый только на этой странице
│       │   │   ├── index.tsx
│       │   │   ├── HeaderSection.module.css
│       │   └── ...               # Остальные компоненты на странице которые используются только 1 раз.
│       └── lib/                  # Вспомогательные функции для страницы (если нужны)