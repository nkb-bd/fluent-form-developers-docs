
<explain-block title="fluentform/maybe_scheduled_jobs">

**Description**

This is a smart background action to process jobs like integration data pushing by schedule time.

**Usage:**
```php 
add_action('fluentform/maybe_scheduled_jobs' ,function () {
   // Do your stuff here
}, 10, 0);
```

**Reference**

`do_action('fluentform/maybe_scheduled_jobs');`

This action is located in `fluentform/boot/globals.php`

</explain-block>

---------------------------------------------------

<explain-block title="fluentform/global_notify_completed">

**Description**

This action fires after completing form integration data pushing process.

**Parameters**
- `$insertId` (int) Submission ID
- `$form` (object) Form Object

**Usage:**
```php 
add_action('fluentform/global_notify_completed' ,function ($insertId, $form) {
   // Do your stuff here
}, 10, 2);
```

**Reference**

`do_action('fluentform/global_notify_completed', $insertId, $form);`

This action is located in `fluentform/app/Services/Integrations/GlobalNotificationManager.php`, `fluentform/app/Services/WPAsync/FluentFormAsyncRequest.php`

</explain-block>

------------------------------------------------

<explain-block title="fluentform/after_submission_api_response_{$status}">

**Description**

This action fires when creating log base on integration API response.

**Parameters**
- `$form`        (object) Form Object
- `$entryId`     (int)    Submission Id
- `$data`        (array)  Integration Date
- `$feed`        (array)  Integration feed value
- `$response`    (array)  Api call response
- `$message`     (string) Response message

**Usage:**
```php 
add_action('fluentform/after_submission_api_response_{$status}', function ($form, $entryId, $data, $feed, $response, $message) {
   // Do your stuff here
}, 10, 6);
```
**Note:** `{$status}` is dynamic status. Replace `{$status}` with one of bellow statuses.
- `success` When response success
- `failed`  When response failed
- `completed`  When response complete

**Reference**

`do_action('fluentform/after_submission_api_response_{$status}', $form, $entryId, $data, $feed, $response, $message);`

This action is located in `fluentform/app/Helpers/IntegrationManagerHelper.php`

</explain-block>

------------------------------------------------

<explain-block title="fluentform/save_global_integration_settings_{$settingsKey}">

**Description**

This action runs when saving a global integration settings with the settings key appended.

**Parameters**
- `$integration`   (array) Integration Settings

**Usage:**
```php 
add_action('fluentform/save_global_integration_settings_{$settingsKey}', function ($integration) {
   // Do your stuff here
}, 10, 1);
```
**Note:** `{$settingsKey}` is dynamic integration key. Replace `{$settingsKey}` with specific integration key.

**Reference**

`do_action('fluentform/save_global_integration_settings_' . $settingsKey, $integration);`

This action is located in `fluentform/app/Http/Controllers/GlobalIntegrationController.php`

</explain-block>

------------------------------------------------

<explain-block title="fluentform/integration_action_result">

**Description**

This action runs after completing an integration process.

**Parameters**
- `$feed` (array) Current Feed
- `$status` (string) Status
- `$note` (string) Note

**Usage:**
```php 
add_action('fluentform/integration_action_result', function ($feed, $status, $note) {
   // Do your stuff here
}, 10, 3);
```


**Reference**

`do_action('fluentform/integration_action_result', $feed, $status, $message);`

This action is located in `fluentformpro/src/Integrations/**/Bootstrap.php`

</explain-block>


