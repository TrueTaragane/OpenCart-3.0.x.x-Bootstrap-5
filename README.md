# 🚀 OpenCart Bootstrap 5 Migration

![Bootstrap](https://img.shields.io/badge/Bootstrap-3%20→%205-7952B3?style=for-the-badge&logo=bootstrap)
![OpenCart](https://img.shields.io/badge/OpenCart-3.0.x.x-1BA1E2?style=for-the-badge&logo=opencart)
![License](https://img.shields.io/badge/License-MIT-green?style=for-the-badge)
![Version](https://img.shields.io/badge/Version-2025-orange?style=for-the-badge)

**Набор инструментов и базовых файлов для миграции OpenCart 3.0.x.x с Bootstrap 3 на Bootstrap 5**

## ⚠️ ВАЖНОЕ ПРЕДУПРЕЖДЕНИЕ

**Это НЕ готовое решение!** Данный проект представляет собой набор инструментов, базовых файлов и документации для начала миграции. **Требуется значительная доработка** под конкретные нужды вашего проекта.

## 📋 Описание

Этот репозиторий содержит **стартовый набор инструментов** для миграции интернет-магазина OpenCart 3.0.x.x с Bootstrap 3 на Bootstrap 5. Проект включает базовые файлы, автоматизированные инструменты миграции и документацию, но **требует основательной доработки** для использования в продакшене.

## ✨ Ключевые возможности

### 🎯 **Готовая тема Bootstrap 5:**

- ✅ **Полностью мигрированная тема** OpenCart с Bootstrap 5
- ✅ **Улучшенная галерея товаров** с модальным окном и навигацией
- ✅ **Нативные Bootstrap 5 карусели** без дополнительных библиотек
- ✅ **Чистая архитектура** без встроенных стилей в template файлах
- ✅ **Bootstrap Icons** - 2000+ современных SVG иконок
- ✅ **Убраны все стикеры** - чистый дизайн без навязчивых бейджей

### 🛠️ **Автоматизированные инструменты:**

- 🤖 **Bootstrap Migration Tool** - автоматическая конвертация тем
- 📊 **Детальные отчеты** о всех изменениях
- 🔧 **Интерактивные скрипты** для Windows и Linux/macOS
- 📦 **Создание архивов** с результатами миграции

### 📚 **Полная документация:**

- 📖 **Пошаговое руководство** по миграции
- 🎯 **Примеры кода** для всех компонентов
- 🔍 **Интерактивный поиск** по классам Bootstrap
- 💡 **Лучшие практики** и рекомендации

## 🚀 Быстрый старт

### ⚠️ ПЕРЕД НАЧАЛОМ РАБОТЫ:

1. **Создайте полную резервную копию** вашего сайта
2. **Тестируйте на копии сайта**, не на продакшене
3. **Будьте готовы к доработке** - это базовые файлы, не готовое решение
4. **Изучите документацию** перед установкой

### Вариант 1: Базовая тема (рекомендуется)

```bash
# 1. Клонируйте репозиторий
git clone https://github.com/your-username/opencart-bootstrap5-migration.git
cd opencart-bootstrap5-migration

# 2. Создайте резервную копию
cp -r /path/to/opencart/catalog /path/to/backup/

# 3. Скопируйте базовые файлы
cp -r catalog_bootstrap5/* /path/to/opencart/catalog/

# 4. ВАЖНО: Доработайте под ваши нужды!
# 5. Протестируйте все функции
# 6. Исправьте возникшие проблемы
```

### Вариант 2: Автоматическая миграция

```bash
# 1. Перейдите в папку с инструментами
cd scripts

# 2. Установите зависимости
npm install

# 3. Запустите миграцию
node bootstrap-migrator.js --input /path/to/theme --output /path/to/migrated_theme
```

### Вариант 3: Интерактивный режим (Windows)

```cmd
# Запустите интерактивный скрипт
scripts\migrate.bat
```

## 📁 Структура проекта

```
opencart-bootstrap5-migration/
├── 📄 index.html                    # Полное руководство по миграции
├── 📁 catalog_bootstrap5/           # Готовая тема Bootstrap 5
│   ├── 📁 view/theme/default/       # Шаблоны и стили
│   ├── 📄 README.md                 # Инструкции по установке
│   └── 📄 *.md                      # Дополнительная документация
├── 📁 scripts/                      # Инструменты автоматической миграции
│   ├── 📄 bootstrap-migrator.js     # Основной скрипт миграции
│   ├── 📄 package.json              # Зависимости Node.js
│   ├── 📄 migrate.bat               # Windows скрипт
│   ├── 📄 migrate.sh                # Linux/macOS скрипт
│   └── 📄 README.md                 # Документация инструментов
└── 📄 README.md                     # Этот файл
```

## 🎯 Что включено

### 🎨 **Готовая тема Bootstrap 5:**

- Полностью обновленные Twig шаблоны
- Современные CSS стили с CSS переменными
- Адаптивный дизайн для всех устройств
- Улучшенная галерея изображений товаров
- Нативные Bootstrap 5 карусели
- Bootstrap Icons (2000+ иконок)

### 🛠️ **Инструменты миграции:**

- Автоматическая замена 100+ CSS классов
- Обновление data-атрибутов Bootstrap
- Миграция иконок Font Awesome → Bootstrap Icons
- Обновление JavaScript API
- Создание детальных отчетов

### 📚 **Документация:**

- Интерактивное руководство с поиском
- Примеры кода для всех компонентов
- Сравнительные таблицы Bootstrap 3 vs 5
- Инструкции по устранению проблем

## 🎨 Новые возможности

### **Улучшенная галерея товаров:**

- Модальное окно для просмотра изображений
- Навигация стрелками и клавиатурой
- Миниатюры для быстрого переключения
- Счетчик изображений
- Адаптивный дизайн

### **Современные карусели:**

- Нативные Bootstrap 5 carousel
- Автоматическое переключение
- Пауза при наведении
- Индикаторы и навигация

### **Чистая архитектура:**

- Убраны встроенные стили из template файлов
- Правильное разделение ответственности
- Централизованные CSS и JavaScript
- Соответствие стандартам OpenCart

## 📊 Сравнение версий

| Функция          | Bootstrap 3      | Bootstrap 5             | Улучшения                    |
| ---------------- | ---------------- | ----------------------- | ---------------------------- |
| **Размер CSS**   | 120KB            | 200KB                   | Больше возможностей          |
| **Размер JS**    | 37KB + jQuery    | 80KB                    | Без зависимости от jQuery    |
| **Иконки**       | Glyphicons (260) | Bootstrap Icons (2000+) | В 8 раз больше               |
| **Адаптивность** | 4 breakpoints    | 6 breakpoints           | Лучшая поддержка устройств   |
| **Кастомизация** | LESS переменные  | CSS переменные          | Нативная поддержка браузеров |
| **Доступность**  | Базовая          | Улучшенная              | WCAG 2.1 совместимость       |

## 🔧 Системные требования

- **OpenCart:** 3.0.x.x (протестировано на 3.0.3.9)
- **PHP:** 7.4+ (рекомендуется 8.1+)
- **Браузеры:** Chrome 90+, Firefox 88+, Safari 14+, Edge 90+
- **Node.js:** 14+ (только для инструментов миграции)

## 📖 Документация

### 📚 Основная документация

- 📄 **[Полное руководство](index.html)** - откройте в браузере
- 📦 **[Подробная установка](INSTALLATION_GUIDE.md)** - пошаговые инструкции
- 🔧 **[Технические требования](TECHNICAL_REQUIREMENTS.md)** - ограничения и требования
- ❓ **[FAQ](FAQ.md)** - часто задаваемые вопросы
- 🔒 **[Безопасность](SECURITY.md)** - политика безопасности

### 🛠️ Инструменты и компоненты

- 🚀 **[Быстрый старт](catalog_bootstrap5/README.md)** - инструкции по установке
- 🛠️ **[Инструменты миграции](scripts/README.md)** - автоматическая конвертация
- 🖼️ **[Галерея изображений](catalog_bootstrap5/GALLERY_IMPROVEMENTS.md)** - возможности и улучшения
- 🪟 **[Установка на Windows](catalog_bootstrap5/WINDOWS_INSTALLATION_GUIDE.md)** - подробная инструкция

### 📋 Дополнительно

- 📝 **[Changelog](CHANGELOG.md)** - история изменений
- 🤝 **[Contributing](CONTRIBUTING.md)** - как внести вклад
- 📄 **[License](LICENSE)** - лицензия MIT
- 🌐 **[English README](README_EN.md)** - English version

## 🧪 Тестирование

### **Готовые тестовые файлы:**

- `catalog_bootstrap5/test_carousel.html` - тест каруселей
- `catalog_bootstrap5/test_gallery.html` - тест галереи товаров
- `scripts/test-migrator.js` - тесты инструментов миграции

### **Браузерное тестирование:**

```javascript
// Откройте консоль браузера и выполните:
console.log("Bootstrap 5:", typeof bootstrap !== "undefined" ? "✅" : "❌");
console.log("Bootstrap Icons:", document.querySelector(".bi") ? "✅" : "❌");
console.log("Карусели:", document.querySelectorAll(".carousel").length);
console.log("Галерея:", document.querySelector("#imageModal") ? "✅" : "❌");
```

## 🤝 Участие в разработке

### **Как внести вклад:**

1. Fork репозитория
2. Создайте feature branch (`git checkout -b feature/amazing-feature`)
3. Commit изменения (`git commit -m 'Add amazing feature'`)
4. Push в branch (`git push origin feature/amazing-feature`)
5. Откройте Pull Request

### **Сообщить об ошибке:**

1. Откройте [Issues](https://github.com/your-username/opencart-bootstrap5-migration/issues)
2. Используйте шаблон bug report
3. Приложите скриншоты и код
4. Укажите версию OpenCart и браузера

## 📈 Roadmap

### **Версия 2.0 (планируется):**

- [ ] Поддержка OpenCart 4.x
- [ ] Темная тема
- [ ] PWA возможности
- [ ] Улучшенная производительность

### **Версия 1.5 (в разработке):**

- [ ] Дополнительные компоненты Bootstrap 5
- [ ] Расширенная галерея с зумом
- [ ] Улучшенные анимации
- [ ] Дополнительные иконки

## 📄 Лицензия

Этот проект распространяется под лицензией MIT. См. файл [LICENSE](LICENSE) для подробностей.

```
MIT License

Copyright (c) 2025 OpenCart Bootstrap 5 Migration

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.
```

## 🌟 Благодарности

- **Bootstrap Team** - за создание отличного фреймворка
- **OpenCart Community** - за вдохновение и обратную связь
- **Contributors** - за помощь в развитии проекта

## 📞 Поддержка

- 🐛 **Issues:** [GitHub Issues](https://github.com/your-username/opencart-bootstrap5-migration/issues)
- 💬 **Discussions:** [GitHub Discussions](https://github.com/your-username/opencart-bootstrap5-migration/discussions)
- 📧 **Email:** support@opencart-bootstrap5.com
- 🌐 **Сайт:** [opencart-bootstrap5.com](https://opencart-bootstrap5.com)

## 📊 Статистика

- ⭐ **GitHub Stars:** Поставьте звезду, если проект полезен!
- 🍴 **Forks:** Создайте fork для своих модификаций
- 📥 **Downloads:** Скачайте готовые файлы
- 🐛 **Issues:** Сообщайте об ошибках и предлагайте улучшения

---

**Сделайте ваш OpenCart современным с Bootstrap 5!** 🎉

[![Скачать готовую тему](https://img.shields.io/badge/Скачать-Готовую%20тему-success?style=for-the-badge)](https://github.com/your-username/opencart-bootstrap5-migration/releases)
[![Открыть документацию](https://img.shields.io/badge/Открыть-Документацию-blue?style=for-the-badge)](https://your-username.github.io/opencart-bootstrap5-migration/)
[![Инструменты миграции](https://img.shields.io/badge/Инструменты-Миграции-orange?style=for-the-badge)](scripts/README.md)
