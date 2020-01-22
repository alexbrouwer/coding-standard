PHP Addition Repository Coding Standard
=======================================

This repository contains all standard coding configuration for all PHP Addition Repository repositories.

Installation
------------

1. Install the library via composer by running:

```bash
composer require --dev par/coding-standard
```

2. Add the following scripts to your `composer.json`: 
```json
{
    "scripts": {
        "cs-check": "phpcs",
        "cs-fix": "phpcbf"
    }
}
```

3. Create file `phpcs.xml` in the root of your repository with content:

```xml
<?xml version="1.0"?>
<ruleset name="PAR Coding Standard">
    <rule ref="./vendor/par/coding-standard/ruleset.xml"/>

    <!-- Paths to check -->
    <file>src</file>
    <file>test</file>
</ruleset>
```

You can add or exclude some locations in that file. For a reference please see:
<https://github.com/squizlabs/PHP_CodeSniffer/wiki/Annotated-ruleset.xml>

Usage
-----

- To run only checks:

```bash
composer cs-check
```

- To automatically fix many CS issues:

```bash
composer cs-fix
```
