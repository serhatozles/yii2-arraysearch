Advanced Array Search
=====================
This function is searching inside of array.

Installation
------------

The preferred way to install this extension is through [composer](http://getcomposer.org/download/).

Either run

```
php composer.phar require --prefer-dist serhatozles/yii2-arraysearch "*"
```

or add

```
"serhatozles/yii2-arraysearch": "*"
```

to the require section of your `composer.json` file.


Usage
-----

Once the extension is installed, simply use it in your code by  :

```php
$query		=	"a='Example World' and b>'2'";

$Array			=	array(
    'a' => array('d' => '2'),
    array('a' => 'Example World','b' => '2'),
    array('c' => '3'),
    array('d' => '4'),
);

$Result = \serhatozles\arraysearch\ArraySearch::q($Array,$query,1);

echo '<pre>';
print_r($Result);
echo '</pre>';

// Output:
// Array
// (
//    [0] => Array
//        (
//            [a] => Example World
//            [b] => 2
//        )
//
// )
```