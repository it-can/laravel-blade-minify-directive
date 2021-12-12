[![PHPStan Level 9](https://img.shields.io/badge/PHPStan-Level%209-brightgreen)](https://phpstan.org/user-guide/rule-levels)
[![GitHub Action Result](https://img.shields.io/github/workflow/status/yamadashy/laravel-blade-minify-directive/Tests?style=flat&logo=github)](https://github.com/yamadashy/laravel-blade-minify-directive/actions)

<div align="center">
  <h3 align="center">Laravel Blade Minify Directive</h3>
  <p align="center">
    <code>@minify</code> directive to partially compress HTML.
  </p>
</div>

# Motivation
There are various minify libraries available, all of which minify the entire page.
However, minifying the whole page may break the design, making it difficult to implement in a large project.

If you want to apply it to a part of the page instead of the whole page, this library is useful.

# Installation
You can install the package via composer:
```
composer require yamadashy/laravel-blade-minify-directive
```

# Usage

Enclose the part you want to minify with `@minify` and `@endminify`.
```blade
<div>
    <div>
        <div>not minified</div>
    </div>
</div>
@minify
<div>
    <div>
        <div>minified</div>
    </div>
</div>
@endminify
<div>
    <div>not minified</div>
</div>
```

Converted like this.
```html
<div>
    <div>
        <div>not minified</div>
    </div>
</div>
<div><div><div>minified</div></div></div>
<div>
    <div>not minified</div>
</div>
```

# License
Distributed under the MIT License. See `LICENSE.txt` for more information.
