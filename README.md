# CSV Builder for PHP
A simple PHP library used to format data into comma-separated values (CSV)

## Installation

```sh
composer require syntaxsolutions/csvbuilder
```

## Example

```php
<?php
// Load Composer's autoloader
require 'vendor/autoload.php';

use CsvBuilder\CsvBuilder;
use CsvBuilder\CsvRow;

$builder = new CsvBuilder();

$headers = new CsvRow();
$headers->addCell("Header 1");
$headers->addCell("Header 2");
$headers->addCell("Header 3");
$builder->addHeaders($headers);

$row = new CsvRow();
$row->addCell("Cell 1");
$row->addCell("Cell 2");
$row->addCell("Cell 3");
$builder->addRow($row);

echo $builder->getBytes();
```