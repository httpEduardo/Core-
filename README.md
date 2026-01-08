# 🍺 Homebrew Core

[![License](https://img.shields.io/badge/license-BSD--2--Clause-blue.svg)](LICENSE.txt)
[![Formulae](https://img.shields.io/badge/formulae-7000%2B-brightgreen.svg)](https://formulae.brew.sh/)
[![GitHub stars](https://img.shields.io/github/stars/Homebrew/homebrew-core.svg)](https://github.com/Homebrew/homebrew-core/stargazers)

**Default formulae for the missing package manager for macOS (or Linux)**

Homebrew Core is the primary repository of formulae for [Homebrew](https://brew.sh), the widely-used package manager that simplifies software installation on macOS and Linux. This repository contains thousands of essential formulae for installing applications, programming languages, libraries, and other tools directly from the terminal.

---

## 📋 Table of Contents

- [Overview](#overview)
- [Installation](#installation)
- [Usage](#usage)
- [API Documentation](#api-documentation)
  - [List All Formulae](#list-all-formulae)
  - [Get Formula Details](#get-formula-details)
- [Resources](#resources)
- [Contributing](#contributing)
- [License](#license)

---

## 🔍 Overview

Homebrew Core provides a comprehensive collection of formulae that are:
- 🔒 **Secure**: Regularly audited and maintained
- ⚡ **Fast**: Optimized for quick installation
- 🌍 **Cross-platform**: Works on macOS and Linux
- 📦 **Comprehensive**: 7,000+ formulae available

The Homebrew Core repository is configured by default when you install Homebrew, which means it's ready to use immediately on macOS and Linux systems.

---

## 🚀 Installation

### Installing Homebrew

If you haven't installed Homebrew yet, run:

```bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

### Installing Formulae

To install any formula from Homebrew Core, use:

```bash
brew install <formula_name>
```

**Example:**

```bash
# Install Python
brew install python

# Install Node.js
brew install node

# Install Git
brew install git
```

### Searching for Formulae

To search for available formulae:

```bash
brew search <keyword>
```

You can also explore all available formulae at [Homebrew Formulae](https://formulae.brew.sh/).

---

## 💡 Usage

### Basic Commands

```bash
# Update Homebrew and upgrade all installed formulae
brew update && brew upgrade

# Install a formula
brew install <formula_name>

# Uninstall a formula
brew uninstall <formula_name>

# List installed formulae
brew list

# Show information about a formula
brew info <formula_name>

# Search for formulae
brew search <keyword>
```

### Advanced Usage

```bash
# Install a specific version
brew install <formula_name>@<version>

# Pin a formula to prevent upgrades
brew pin <formula_name>

# Unpin a formula
brew unpin <formula_name>

# Check for issues
brew doctor
```

---

## 📡 API Documentation

Homebrew provides a public API for accessing detailed information about formulae programmatically. The API enables you to:

- ✅ List all formulae available in Homebrew Core and Homebrew Cask
- ✅ Query metadata for specific formulae (versions, dependencies, analytics)
- ✅ Access analytics events grouped by formula name or Cask token

### List All Formulae

**Endpoint:**
```
GET https://formulae.brew.sh/api/formula.json
```

**Description:** Returns a complete list of all formulae available in Homebrew Core.

**Example:**
```bash
curl https://formulae.brew.sh/api/formula.json
```

### Get Formula Details

**Endpoint:**
```
GET https://formulae.brew.sh/api/formula/${FORMULA}.json
```

**Description:** Returns detailed information about a specific formula, including:
- Current version
- Dependencies
- Installation requirements
- Analytics data
- Homepage and documentation links

**Example:**
```bash
# Get information about Python
curl https://formulae.brew.sh/api/formula/python.json

# Get information about Node.js
curl https://formulae.brew.sh/api/formula/node.json
```

**Response Structure:**
```json
{
  "name": "python",
  "full_name": "python",
  "tap": "homebrew/core",
  "oldname": null,
  "aliases": ["python@3", "python3"],
  "versioned_formulae": [],
  "desc": "Interpreted, interactive, object-oriented programming language",
  "license": "Python-2.0",
  "homepage": "https://www.python.org/",
  "versions": {
    "stable": "3.11.0",
    "head": null,
    "bottle": true
  },
  "dependencies": [...],
  "build_dependencies": [...]
}
```

---

## 📚 Resources

Homebrew is more than just a package manager. It offers extensive documentation and resources for:

- 📖 [Official Documentation](https://docs.brew.sh/)
- 🐛 [Troubleshooting Guide](https://docs.brew.sh/Troubleshooting)
- 🔧 [Formula Cookbook](https://docs.brew.sh/Formula-Cookbook)
- 💬 [Community Discussion](https://github.com/Homebrew/discussions)
- 🔒 [Security Policy](https://github.com/Homebrew/brew/security/policy)
- ❤️ [Donations](https://github.com/Homebrew/brew#donations)
- 📰 [Blog](https://brew.sh/blog/)

For complete information about Homebrew itself, visit the [official Homebrew repository](https://github.com/Homebrew/brew).

---

## 🤝 Contributing

We welcome contributions from the community! Whether you want to:

- 🐛 Report a bug
- ✨ Add a new formula
- 🔄 Update an existing formula
- 📝 Improve documentation

Please read our [Contributing Guidelines](CONTRIBUTING.md) to get started.

### Quick Start for Contributors

```bash
# Create a new formula
brew create <URL>

# Edit an existing formula
brew edit <formula_name>

# Test your changes
brew install --build-from-source <formula_name>
brew test <formula_name>
brew audit --strict <formula_name>
```

---

## 📄 License

Homebrew Core is licensed under the [BSD 2-Clause License](LICENSE.txt).

```
Copyright (c) 2009-present, Homebrew contributors
All rights reserved.
```

See the [LICENSE.txt](LICENSE.txt) file for full license text.

---

<div align="center">

**Made with ❤️ by the [Homebrew Community](https://github.com/Homebrew)**

[Website](https://brew.sh) • [Documentation](https://docs.brew.sh) • [Forum](https://github.com/Homebrew/discussions) • [API](https://formulae.brew.sh/docs/api/)

</div>
