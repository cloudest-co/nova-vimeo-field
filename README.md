# Laravel Nova 4.0 Vimeo Field

## Installation

`composer require cloudest/vimeo`

## Usage
```php
use Cloudest\Vimeo;

Vimeo::make('Vimeo field name'),
```
The field extends the base Laravel\Nova\Fields\Field, so all the usual methods are available.

## Options

### With meta
```php
use Cloudest\Vimeo;

Vimeo::make('Vimeo field name')
    ->withMeta([
        'options' => [
            'width' => 640,
            'height' => 360,
        ]
    ]);
```

## License
The MIT License (MIT). Please see [License File](LICENSE) for more information.

