# Execute code quality analysis a Drupal 8+ instance

This GitHub action runs code quality analysis on custom written code located in `web/modules/custom` and `web/themes/custom`


In your project you are required to install the correct tools:

```shell
composer require --dev  drupal/coder overtrue/phplint phpmd/phpmd
```