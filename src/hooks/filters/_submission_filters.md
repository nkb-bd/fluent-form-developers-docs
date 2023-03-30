<explain-block title="fluentform/insert_response_data">
If you want to add or remove dashboard stats cards then you can use this filter.

**Parameters**

- `$formData` Form Data
- `$formId` Form Id
- `$inputConfigs` Form Inputs

**Usage:**

```php 
/*
* Filter Insert Data
*/
add_filter('fluentform/insert_response_data', function($formData, $formId, $inputConfigs) {
  
   return $formData;
});
```
</explain-block>
