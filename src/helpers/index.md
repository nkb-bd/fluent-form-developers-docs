## Helper Classes

Fluent Forms provides few helper classes that you can interact easily to build advanced functionalities on your plugin.
Many of these functions are used by the plugin itself; however, you are free to use them in your own addon if you find them convenient.


# Fluent Forms Core Helper Class

- Class with Namespace: `\FluentForm\App\Helpers\Helper`
- Method Types: `static`

### Helper::getProfileSections()

The `Helper::getForms` method returns all forms with form id as keyed array.

```php 
$forms = \FluentForm\App\Helpers\Helper::getForms();
/*
[
    [0] => Select a Fluent Forms
    [284] => Blank Form (#284) (284)
    [283] => Contact Form Demo (#16) (283)
    [156] => Post Form (#156) (156)
    [5] => Conversational Form (#5) (5)
    [2] => Step form (2)
    [1] => Contact Form Demo (1)
]
*/
```



