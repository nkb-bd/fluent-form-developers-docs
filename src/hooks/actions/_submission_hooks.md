<explain-block title="fluentform/before_insert_submission">
This action runs when a contact created

**Parameters**
- `$insertData` Insert Model
- `$data` Form Data
- `$form` Form Object

**Usage:**
```php 
add_action('fluentform/before_insert_submission', function($insertData, $data, $form) {
   // Do whatever you want before inserting a submission
}, 10, 3);
```
</explain-block>

<explain-block title="fluentform/submission_inserted">
This action runs after a submission is inserted 

**Parameters**
- `$submissionId` Submission ID
- `$formData` Form Data
- `$form` Form Object

**Usage:**
```php 
add_action('fluentform/submission_inserted', function($submissionId, $formData, $form) {
   // Do whatever you want with the new submission
}, 10, 3);
```
</explain-block>

<explain-block title="fluentform/before_submission_confirmation">
This action runs when tags have been added to a contact

**Parameters**
- `$submissionId` Submission ID
- `$formData` Form  Data
- `$form` Form Object

**Usage:**
```php 
add_action('fluentform/before_submission_confirmation', function($submissionId, $formData, $form) {
   // Do whatever you want here
}, 10, 3);
```
</explain-block>

<explain-block title="fluentform/before_form_actions_processing">
This action fires after form submission and before processing the form’s additional actions. If you want to do any task before form submission

**Parameters**
- `$submissionId` Submission ID
- `$formData` Form  Data
- `$form` Form Object

**Usage:**
```php 
add_action('fluentform_before_form_actions_processing', function($submissionId, $formData, $form){  
     // Do your stuff here
}, 10, 3)
```
</explain-block>
<explain-block title="fluentform/before_insert_payment_form">
If the form has payment then this action will be fired before submission. You can use this to do your payment related custom tasks.
**Parameters**
- `$insertData` Form response data
- `$formData` Form Raw Data
- `$form` Form Object

**Usage:**
```php 
add_action('fluentform/before_insert_payment_form', 'custom_funtion',function ($insertData, $formRawData, $form){
   // Do your stuff here
}, 10, 3);

```
</explain-block>


