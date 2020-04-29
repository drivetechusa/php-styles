### Add repository to composer.json
    "repositories": [
      {
        "type": "vcs",
        "url": "https://github.com/drivetechusa/php-styles"
      }
    ]

### Composer require
    composer require drivetechusa/php-styles --dev

### Create file .php_cs.dist

    <?php
      $finder = PhpCsFixer\Finder::create()
        ->in([
            __DIR__.'/app',
            __DIR__.'/config',
            __DIR__.'/database',
            __DIR__.'/routes',
            __DIR__.'/tests',
        ]);
      return Drivetechusa\styles($finder);
    >

### Run the following command

./vendor/bin/php-cs-fixer fix