# Execute code quality analysis a Drupal 10+ instance

This GitHub action runs code quality analysis on custom written code located in `web/modules/custom` and `web/themes/custom`.

It includes PHPLint, PHPCS, PHPMD and PHPStan.

Usage:
```yaml
jobs:
  qa-code:
    name: 'Check code quality'
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v3
        with:
          fetch-depth: 1
      - uses: eaudeweb/drupal-install-action@v1.1
      - uses: eaudeweb/drupal-code-qa-action@2.x
        with:
          phplint: 'true'
          phpmd: 'true'
          phpcs: 'true'
          phpcs_standards: 'Drupal,DrupalPractice'
          phpcs_extensions: 'php,module,inc,install,profile,theme,test,info,yml'
          phpstan: 'true'
          phpstan_level: '9'
```