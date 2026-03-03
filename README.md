# ext-i18n-framework

[![npm version](https://img.shields.io/npm/v/@zovo/ext-i18n-framework)](https://npmjs.com/package/@zovo/ext-i18n-framework)
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](https://opensource.org/licenses/MIT)
[![TypeScript](https://img.shields.io/badge/TypeScript-5.x-blue.svg)](https://www.typescriptlang.org/)
[![CI Status](https://github.com/theluckystrike/ext-i18n-framework/actions/workflows/ci.yml/badge.svg)](https://github.com/theluckystrike/ext-i18n-framework/actions)
[![Discord](https://img.shields.io/badge/Discord-Zovo-blueviolet.svg?logo=discord)](https://discord.gg/zovo)
[![Website](https://img.shields.io/badge/Website-zovo.one-blue)](https://zovo.one)
[![GitHub Stars](https://img.shields.io/github/stars/theluckystrike/ext-i18n-framework?style=social)](https://github.com/theluckystrike/ext-i18n-framework)

> Full i18n framework for Chrome extensions with multi-language support.

Part of the [Zovo](https://zovo.one) family of privacy-first Chrome extensions and developer tools.

## Overview

`ext-i18n-framework` is a comprehensive internationalization (i18n) framework designed specifically for Chrome extensions. It provides robust support for multiple languages, locale detection, and dynamic language switching.

## Features

- ✅ **Multi-language Support** - Support for unlimited languages
- ✅ **Locale Detection** - Automatic browser locale detection
- ✅ **Dynamic Switching** - Change languages at runtime
- ✅ **TypeScript Support** - Fully typed for better developer experience
- ✅ **MV3 Compatible** - Works with Manifest V3 extensions
- ✅ **Privacy-First** - No data collection, all local

## Installation

### From npm

```bash
npm install @zovo/ext-i18n-framework
```

### From Source

```bash
# Clone the repository
git clone https://github.com/theluckystrike/ext-i18n-framework.git
cd ext-i18n-framework

# Install dependencies
npm install

# Build the project
npm run build
```

## Usage

### Basic Usage

```typescript
import { I18n, initI18n } from '@zovo/ext-i18n-framework';

// Initialize i18n with default locale
await initI18n({
  defaultLocale: 'en',
  locales: ['en', 'es', 'fr', 'de']
});

// Get a translation
const greeting = I18n.t('greeting.hello');
console.log(greeting); // "Hello!"
```

### Setting Locale

```typescript
import { I18n, setLocale } from '@zovo/ext-i18n-framework';

// Change locale
await setLocale('es');

// Translations now use Spanish
console.log(I18n.t('greeting.hello')); // "¡Hola!"
```

### Adding Translations

```typescript
import { addTranslations } from '@zovo/ext-i18n-framework';

addTranslations('fr', {
  greeting: {
    hello: 'Bonjour!',
    goodbye: 'Au revoir!'
  }
});
```

## API Reference

### Functions

| Function | Description |
|----------|-------------|
| `initI18n(options)` | Initialize the i18n framework |
| `t(key)` | Get a translation by key |
| `setLocale(locale)` | Change the current locale |
| `getLocale()` | Get the current locale |
| `addTranslations(locale, translations)` | Add translations for a locale |

## Related Packages

This package is part of the Zovo i18n ecosystem:

- [ext-i18n-api](https://github.com/theluckystrike/ext-i18n-api) - i18n API utilities
- [ext-i18n-locale](https://github.com/theluckystrike/ext-i18n-locale) - Locale detection and management
- [ext-i18n-pro](https://github.com/theluckystrike/ext-i18n-pro) - Pro i18n features
- [ext-localization](https://github.com/theluckystrike/ext-localization) - Localization utilities

## Contributing

Contributions are welcome! Please follow these steps:

1. **Fork** the repository
2. **Create** a feature branch: `git checkout -b feature/i18n-improvement`
3. **Make** your changes
4. **Test** your changes: `npm test`
5. **Commit** your changes: `git commit -m 'Add new feature'`
6. **Push** to the branch: `git push origin feature/i18n-improvement`
7. **Submit** a Pull Request

### Development Setup

```bash
# Clone the repository
git clone https://github.com/theluckystrike/ext-i18n-framework.git
cd ext-i18n-framework

# Install dependencies
npm install

# Run tests
npm test

# Build
npm run build
```

## Built by Zovo

Part of the [Zovo](https://zovo.one) developer tools family — privacy-first Chrome extensions built by developers, for developers.

## See Also

### Related Zovo Repositories

- [zovo-extension-template](https://github.com/theluckystrike/zovo-extension-template) - Boilerplate for building privacy-first Chrome extensions
- [zovo-types-webext](https://github.com/theluckystrike/zovo-types-webext) - Comprehensive TypeScript type definitions for browser extensions
- [zovo-permissions-scanner](https://github.com/theluckystrike/zovo-permissions-scanner) - Privacy scanner for Chrome extensions
- [zovo-indexer](https://github.com/theluckystrike/zovo-indexer) - Indexing service for Zovo extensions

### Zovo Chrome Extensions

- [Zovo Tab Manager](https://chrome.google.com/webstore/detail/zovo-tab-manager) - Manage tabs efficiently
- [Zovo Focus](https://chrome.google.com/webstore/detail/zovo-focus) - Block distractions
- [Zovo Permissions Scanner](https://chrome.google.com/webstore/detail/zovo-permissions-scanner) - Check extension privacy grades

Visit [zovo.one](https://zovo.one) for more information.

## License

MIT - [Zovo](https://zovo.one)

---

*Built by developers, for developers. No compromises on privacy.*
