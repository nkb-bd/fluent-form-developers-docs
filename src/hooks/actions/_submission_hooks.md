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
});
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
});
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
}, 10, 2);
```
</explain-block>


