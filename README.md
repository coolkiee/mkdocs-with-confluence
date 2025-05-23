# mkdocs-with-confluence

![PyPI](https://img.shields.io/pypi/v/mkdocs-with-confluence)
[![Build Status](https://app.travis-ci.com/pawelsikora/mkdocs-with-confluence.svg?token=Nxwjs6L2kEPqZeJARZzo&branch=main)](https://app.travis-ci.com/pawelsikora/mkdocs-with-confluence)
[![codecov](https://codecov.io/gh/pawelsikora/mkdocs-with-confluence/branch/master/graph/badge.svg)](https://codecov.io/gh/pawelsikora/mkdocs-with-confluence)
![PyPI - Downloads](https://img.shields.io/pypi/dm/mkdocs-with-confluence)
![GitHub contributors](https://img.shields.io/github/contributors/pawelsikora/mkdocs-with-confluence)
![PyPI - License](https://img.shields.io/pypi/l/mkdocs-with-confluence)
![PyPI - Python Version](https://img.shields.io/pypi/pyversions/mkdocs-with-confluence)

A MkDocs plugin that converts Markdown documentation to Confluence markup and publishes it to Confluence pages.

## ✨ Features

- Seamless Markdown to Confluence conversion
- Supports nested page hierarchies
- Environment-aware deployment
- Dry-run mode for testing
- Verbose logging for debugging

## 📦 Installation

Install the plugin using pip:

```bash
pip install mkdocs-with-confluence
```

Enable the plugin in your mkdocs.yml:
plugins:
  - search
  - mkdocs-with-confluence

More information about plugins in the [MkDocs documentation: mkdocs-plugins](https://www.mkdocs.org/user-guide/plugins/).

## Usage

Use following config and adjust it according to your needs:

plugins:
  - mkdocs-with-confluence:
      host_url: "https://your-domain.atlassian.net/rest/api/content"
      space: "SPACE_KEY"  # e.g., "DOCS"
      parent_page_name: "Home"
      username: "your@email.com"  # Recommended to use API token
      password: "your-api-token"  # Generate at: https://id.atlassian.com/manage-profile/security/api-tokens
      enabled_if_env: "MKDOCS_TO_CONFLUENCE"  # Optional safety switch
      dryrun: true              # Test mode (default)
      # verbose: true           # Enable detailed logging
      # debug: true             # Enable debug mode


### Requirements
Python 3.6+
md2cf>=2.0.0
mistune>=2.0.0
mimetypes (standard library)
