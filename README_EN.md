# 🚀 OpenCart Bootstrap 5 Migration

![Bootstrap](https://img.shields.io/badge/Bootstrap-3%20→%205-7952B3?style=for-the-badge&logo=bootstrap)
![OpenCart](https://img.shields.io/badge/OpenCart-3.0.x.x-1BA1E2?style=for-the-badge&logo=opencart)
![License](https://img.shields.io/badge/License-MIT-green?style=for-the-badge)
![Version](https://img.shields.io/badge/Version-2025-orange?style=for-the-badge)

**Toolkit and base files for migrating OpenCart 3.0.x.x from Bootstrap 3 to Bootstrap 5**

## ⚠️ IMPORTANT WARNING

**This is NOT a ready-to-use solution!** This project is a toolkit of base files and documentation to start migration. **Significant customization required** for your specific project needs.

## 📋 Description

This repository contains a **starter toolkit** for migrating OpenCart 3.0.x.x e-commerce stores from outdated Bootstrap 3 to modern Bootstrap 5. The project includes base files, automated migration tools, and documentation, but **requires substantial development** for production use.

## ✨ Key Features

### 🎯 **Base Bootstrap 5 Theme:**

- ✅ **Basic migrated theme** OpenCart with Bootstrap 5
- ✅ **Enhanced product gallery** with modal window and navigation
- ✅ **Native Bootstrap 5 carousels** without additional libraries
- ✅ **Clean architecture** without inline styles in template files
- ✅ **Bootstrap Icons** - 2000+ modern SVG icons
- ✅ **Removed all stickers** - clean design without intrusive badges

### 🛠️ **Automated Tools:**

- 🤖 **Bootstrap Migration Tool** - automatic theme conversion
- 📊 **Detailed reports** of all changes
- 🔧 **Interactive scripts** for Windows and Linux/macOS
- 📦 **Archive creation** with migration results

### 📚 **Complete Documentation:**

- 📖 **Step-by-step guide** for migration
- 🎯 **Code examples** for all components
- 🔍 **Interactive search** for Bootstrap classes
- 💡 **Best practices** and recommendations

## 🚀 Quick Start

### Option 1: Base Theme (recommended)

```bash
# 1. Clone repository
git clone https://github.com/your-username/opencart-bootstrap5-migration.git
cd opencart-bootstrap5-migration

# 2. Create backup
cp -r /path/to/opencart/catalog /path/to/backup/

# 3. Copy base files
cp -r catalog_bootstrap5/* /path/to/opencart/catalog/

# 4. IMPORTANT: Customize for your needs!
```

### Option 2: Automatic Migration

```bash
# 1. Navigate to tools folder
cd scripts

# 2. Install dependencies
npm install

# 3. Run migration
node bootstrap-migrator.js --input /path/to/theme --output /path/to/migrated_theme
```

### Option 3: Interactive Mode (Windows)

```cmd
# Run interactive script
scripts\migrate.bat
```

## 📁 Project Structure

```
opencart-bootstrap5-migration/
├── 📄 index.html                    # Complete migration guide
├── 📁 catalog_bootstrap5/           # Base Bootstrap 5 theme
│   ├── 📁 view/theme/default/       # Templates and styles
│   ├── 📄 README.md                 # Installation instructions
│   └── 📄 *.md                      # Additional documentation
├── 📁 scripts/                      # Automated migration tools
│   ├── 📄 bootstrap-migrator.js     # Main migration script
│   ├── 📄 package.json              # Node.js dependencies
│   ├── 📄 migrate.bat               # Windows script
│   ├── 📄 migrate.sh                # Linux/macOS script
│   └── 📄 README.md                 # Tools documentation
└── 📄 README.md                     # This file
```

## 🎯 What's Included

### 🎨 **Base Bootstrap 5 Theme:**

- Basic updated Twig templates
- Modern CSS styles with CSS variables
- Responsive design for all devices
- Enhanced product image gallery
- Native Bootstrap 5 carousels
- Bootstrap Icons (2000+ icons)

### 🛠️ **Migration Tools:**

- Automatic replacement of 100+ CSS classes
- Bootstrap data-attributes updates
- Font Awesome → Bootstrap Icons migration
- JavaScript API updates
- Detailed report generation

### 📚 **Documentation:**

- Interactive guide with search
- Code examples for all components
- Bootstrap 3 vs 5 comparison tables
- Troubleshooting instructions

## 🎨 New Features

### **Enhanced Product Gallery:**

- Modal window for image viewing
- Arrow and keyboard navigation
- Thumbnails for quick switching
- Image counter
- Responsive design

### **Modern Carousels:**

- Native Bootstrap 5 carousel
- Automatic switching
- Pause on hover
- Indicators and navigation

### **Clean Architecture:**

- Removed inline styles from template files
- Proper separation of concerns
- Centralized CSS and JavaScript
- OpenCart standards compliance

## 📊 Version Comparison

| Feature           | Bootstrap 3      | Bootstrap 5             | Improvements           |
| ----------------- | ---------------- | ----------------------- | ---------------------- |
| **CSS Size**      | 120KB            | 200KB                   | More features          |
| **JS Size**       | 37KB + jQuery    | 80KB                    | No jQuery dependency   |
| **Icons**         | Glyphicons (260) | Bootstrap Icons (2000+) | 8x more icons          |
| **Responsive**    | 4 breakpoints    | 6 breakpoints           | Better device support  |
| **Customization** | LESS variables   | CSS variables           | Native browser support |
| **Accessibility** | Basic            | Enhanced                | WCAG 2.1 compliance    |

## 🔧 System Requirements

- **OpenCart:** 3.0.x.x (tested on 3.0.3.9)
- **PHP:** 7.4+ (recommended 8.1+)
- **Browsers:** Chrome 90+, Firefox 88+, Safari 14+, Edge 90+
- **Node.js:** 14+ (for migration tools only)

## 📖 Documentation

- 📄 **[Complete Guide](index.html)** - open in browser
- 🚀 **[Quick Start](catalog_bootstrap5/README.md)** - installation instructions
- 🛠️ **[Migration Tools](scripts/README.md)** - automatic conversion
- 🖼️ **[Image Gallery](catalog_bootstrap5/GALLERY_IMPROVEMENTS.md)** - features and improvements
- 🪟 **[Windows Installation](catalog_bootstrap5/WINDOWS_INSTALLATION_GUIDE.md)** - detailed instructions

## 🧪 Testing

### **Ready Test Files:**

- `catalog_bootstrap5/test_carousel.html` - carousel tests
- `catalog_bootstrap5/test_gallery.html` - product gallery tests
- `scripts/test-migrator.js` - migration tools tests

### **Browser Testing:**

```javascript
// Open browser console and execute:
console.log("Bootstrap 5:", typeof bootstrap !== "undefined" ? "✅" : "❌");
console.log("Bootstrap Icons:", document.querySelector(".bi") ? "✅" : "❌");
console.log("Carousels:", document.querySelectorAll(".carousel").length);
console.log("Gallery:", document.querySelector("#imageModal") ? "✅" : "❌");
```

## 🤝 Contributing

### **How to Contribute:**

1. Fork the repository
2. Create feature branch (`git checkout -b feature/amazing-feature`)
3. Commit changes (`git commit -m 'Add amazing feature'`)
4. Push to branch (`git push origin feature/amazing-feature`)
5. Open Pull Request

### **Report a Bug:**

1. Open [Issues](https://github.com/your-username/opencart-bootstrap5-migration/issues)
2. Use bug report template
3. Attach screenshots and code
4. Specify OpenCart version and browser

## 📈 Roadmap

### **Version 2.0 (planned):**

- [ ] OpenCart 4.x support
- [ ] Dark theme
- [ ] PWA capabilities
- [ ] Enhanced performance

### **Version 1.5 (in development):**

- [ ] Additional Bootstrap 5 components
- [ ] Extended gallery with zoom
- [ ] Improved animations
- [ ] Additional icons

## 📄 License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

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

## 🌟 Acknowledgments

- **Bootstrap Team** - for creating an excellent framework
- **OpenCart Community** - for inspiration and feedback
- **Contributors** - for helping develop the project

## 📞 Support

- 🐛 **Issues:** [GitHub Issues](https://github.com/your-username/opencart-bootstrap5-migration/issues)
- 💬 **Discussions:** [GitHub Discussions](https://github.com/your-username/opencart-bootstrap5-migration/discussions)
- 📧 **Email:** support@opencart-bootstrap5.com
- 🌐 **Website:** [opencart-bootstrap5.com](https://opencart-bootstrap5.com)

## 📊 Statistics

- ⭐ **GitHub Stars:** Star if the project is useful!
- 🍴 **Forks:** Create fork for your modifications
- 📥 **Downloads:** Download base files
- 🐛 **Issues:** Report bugs and suggest improvements

---

**Make your OpenCart modern with Bootstrap 5!** 🎉

[![Download Base Theme](https://img.shields.io/badge/Download-Base%20Theme-success?style=for-the-badge)](https://github.com/your-username/opencart-bootstrap5-migration/releases)
[![Open Documentation](https://img.shields.io/badge/Open-Documentation-blue?style=for-the-badge)](https://your-username.github.io/opencart-bootstrap5-migration/)
[![Migration Tools](https://img.shields.io/badge/Migration-Tools-orange?style=for-the-badge)](scripts/README.md)
