# 📦 Подробное руководство по установке

## 🎯 Обзор процесса установки

Этот документ содержит пошаговые инструкции по установке и настройке OpenCart Bootstrap 5 Migration toolkit.

## ⚠️ ПЕРЕД НАЧАЛОМ

### Обязательные шаги:

1. **Создайте полную резервную копию** вашего сайта
2. **Настройте тестовую среду** - НЕ устанавливайте на продакшен
3. **Убедитесь в совместимости** вашей версии OpenCart
4. **Проверьте системные требования**

### Проверка системных требований:

```bash
# Проверка версии PHP
php -v

# Проверка версии OpenCart (в админке)
# Система → Настройки → Сервер → Версия

# Проверка Node.js (для инструментов миграции)
node --version
npm --version
```

## 🚀 Способ 1: Использование готовых файлов

### Шаг 1: Подготовка

```bash
# 1. Создайте рабочую директорию
mkdir opencart-migration
cd opencart-migration

# 2. Клонируйте репозиторий
git clone https://github.com/your-username/opencart-bootstrap5-migration.git
cd opencart-bootstrap5-migration
```

### Шаг 2: Резервное копирование

```bash
# Создайте полную резервную копию
cp -r /path/to/your/opencart /path/to/backup/opencart_backup_$(date +%Y%m%d)

# Или используйте tar для сжатия
tar -czf opencart_backup_$(date +%Y%m%d).tar.gz /path/to/your/opencart
```

### Шаг 3: Установка базовых файлов

```bash
# Скопируйте файлы темы
cp -r catalog_bootstrap5/view /path/to/your/opencart/catalog/

# Проверьте права доступа
chmod -R 755 /path/to/your/opencart/catalog/view
```

### Шаг 4: Обновление Bootstrap файлов

1. **Скачайте Bootstrap 5.3.3:**

   - Перейдите на [getbootstrap.com](https://getbootstrap.com/)
   - Скачайте compiled CSS and JS
   - Распакуйте в `catalog/view/theme/default/stylesheet/bootstrap/`

2. **Скачайте Bootstrap Icons:**
   - Перейдите на [icons.getbootstrap.com](https://icons.getbootstrap.com/)
   - Скачайте font files
   - Распакуйте в `catalog/view/theme/default/stylesheet/bootstrap-icons/`

### Шаг 5: Первичная проверка

```bash
# Откройте сайт в браузере
# Проверьте основные страницы:
# - Главная страница
# - Каталог товаров
# - Страница товара
# - Корзина
# - Оформление заказа
```

## 🛠️ Способ 2: Автоматическая миграция

### Шаг 1: Установка Node.js

#### Windows:

```cmd
# Скачайте с https://nodejs.org/
# Запустите установщик
# Перезагрузите командную строку
```

#### Linux (Ubuntu/Debian):

```bash
# Обновите пакеты
sudo apt update

# Установите Node.js
sudo apt install nodejs npm

# Проверьте установку
node --version
npm --version
```

#### macOS:

```bash
# Используя Homebrew
brew install node

# Или скачайте с nodejs.org
```

### Шаг 2: Подготовка инструментов

```bash
# Перейдите в папку скриптов
cd scripts

# Установите зависимости
npm install

# Проверьте установку
node bootstrap-migrator.js --help
```

### Шаг 3: Запуск миграции

#### Интерактивный режим (рекомендуется):

```bash
# Windows
migrate.bat

# Linux/macOS
./migrate.sh
```

#### Командная строка:

```bash
# Базовая миграция
node bootstrap-migrator.js --input /path/to/your/theme --output /path/to/migrated_theme

# С дополнительными опциями
node bootstrap-migrator.js \
  --input /path/to/your/theme \
  --output /path/to/migrated_theme \
  --backup \
  --report \
  --zip
```

### Шаг 4: Проверка результатов

```bash
# Проверьте созданные файлы
ls -la /path/to/migrated_theme

# Просмотрите отчет о миграции
cat /path/to/migrated_theme/migration_report.txt

# Проверьте архив (если создавался)
ls -la *.zip
```

## 🔧 Настройка и доработка

### Обязательные настройки:

1. **Обновите пути к файлам Bootstrap:**

```php
// В catalog/view/theme/default/template/common/header.twig
<link href="catalog/view/theme/default/stylesheet/bootstrap/css/bootstrap.min.css" rel="stylesheet">
<link href="catalog/view/theme/default/stylesheet/bootstrap-icons/bootstrap-icons.css" rel="stylesheet">
```

2. **Проверьте JavaScript:**

```javascript
// Убедитесь, что Bootstrap 5 JS загружается
<script src="catalog/view/theme/default/js/bootstrap/js/bootstrap.bundle.min.js"></script>
```

3. **Обновите конфигурацию:**

```php
// В config.php добавьте (если нужно)
define('BOOTSTRAP_VERSION', '5.3.3');
```

### Рекомендуемые настройки:

1. **Создайте кастомный CSS файл:**

```css
/* catalog/view/theme/default/stylesheet/custom.css */
:root {
  --primary-color: #007bff;
  --secondary-color: #6c757d;
  /* Ваши кастомные переменные */
}

/* Ваши кастомные стили */
.custom-component {
  /* ... */
}
```

2. **Настройте мета-теги:**

```html
<!-- В header.twig -->
<meta name="viewport" content="width=device-width, initial-scale=1" />
<meta name="theme-color" content="#007bff" />
```

## 🧪 Тестирование

### Автоматическое тестирование:

```bash
# Запустите тесты инструментов
cd scripts
node test-migrator.js

# Проверьте валидность HTML
# Используйте онлайн валидаторы или локальные инструменты
```

### Ручное тестирование:

1. **Функциональное тестирование:**

   - [ ] Регистрация пользователя
   - [ ] Авторизация
   - [ ] Добавление товара в корзину
   - [ ] Оформление заказа
   - [ ] Поиск товаров
   - [ ] Фильтрация каталога

2. **Визуальное тестирование:**

   - [ ] Главная страница
   - [ ] Каталог товаров
   - [ ] Страница товара
   - [ ] Корзина
   - [ ] Личный кабинет
   - [ ] Страницы информации

3. **Адаптивное тестирование:**
   - [ ] Мобильные устройства (320px+)
   - [ ] Планшеты (768px+)
   - [ ] Десктоп (1200px+)
   - [ ] Большие экраны (1400px+)

### Тестовые файлы:

```bash
# Откройте в браузере
catalog_bootstrap5/test_gallery.html
catalog_bootstrap5/test_carousel.html

# Проверьте консоль браузера на ошибки
```

## 🐛 Устранение проблем

### Частые проблемы:

1. **Стили не применяются:**

```bash
# Проверьте пути к файлам
# Очистите кеш браузера
# Проверьте права доступа к файлам
chmod -R 755 catalog/view/theme/default/stylesheet/
```

2. **JavaScript не работает:**

```javascript
// Проверьте загрузку Bootstrap JS
console.log(typeof bootstrap);

// Проверьте ошибки в консоли
// F12 → Console
```

3. **Галерея изображений не работает:**

```html
<!-- Убедитесь, что модальное окно присутствует -->
<div class="modal fade" id="imageModal">
  <!-- ... -->
</div>
```

4. **Карусели не работают:**

```html
<!-- Проверьте data-атрибуты Bootstrap 5 -->
<div class="carousel slide" data-bs-ride="carousel">
  <!-- ... -->
</div>
```

### Логи и отладка:

```bash
# Проверьте логи веб-сервера
tail -f /var/log/apache2/error.log
tail -f /var/log/nginx/error.log

# Проверьте логи PHP
tail -f /var/log/php/error.log

# Включите отладку в OpenCart
# В config.php:
define('DEBUG', true);
```

## 📊 Мониторинг производительности

### Инструменты для проверки:

1. **Google PageSpeed Insights**
2. **GTmetrix**
3. **WebPageTest**
4. **Lighthouse** (встроен в Chrome)

### Оптимизация:

```bash
# Сжатие CSS и JS
npm install -g clean-css-cli uglify-js

# Сжатие CSS
cleancss -o style.min.css style.css

# Сжатие JS
uglifyjs script.js -o script.min.js
```

## 📞 Получение поддержки

### Если возникли проблемы:

1. **Проверьте FAQ** в документации
2. **Изучите известные проблемы** в TECHNICAL_REQUIREMENTS.md
3. **Создайте Issue** на GitHub с подробным описанием
4. **Приложите логи** и скриншоты

### Информация для Issue:

```
**Окружение:**
- OpenCart версия: 3.0.3.9
- PHP версия: 8.1
- Браузер: Chrome 120
- ОС: Ubuntu 20.04

**Проблема:**
[Подробное описание]

**Шаги для воспроизведения:**
1. ...
2. ...
3. ...

**Ожидаемое поведение:**
[Что должно происходить]

**Фактическое поведение:**
[Что происходит на самом деле]

**Скриншоты:**
[Приложите скриншоты]

**Логи:**
[Приложите соответствующие логи]
```

---

**Удачной установки!** 🚀

Помните: это базовый набор инструментов, требующий доработки под ваши конкретные нужды.
