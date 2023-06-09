<explain-block title="fluentform/email_summary_config">

You can use this filter to modify email summary configuration.

**Parameters**

- `$config` (array) Email Summary Configuration

**Usage**

```php
add_filter('fluentform/email_summary_config', function ($config) {
    // Do your stuff here
    
    return $config;
}, 10, 1);

```

**Reference**

`apply_filters('fluentform/email_summary_config', $config);`

This filter is located in FluentForm\App\Services\Scheduler\Scheduler -> processEmailReport()

</explain-block>

<explain-block title="fluentform/email_summary_body">

You can use this filter to modify email body.

**Parameters**

- `$emailBody` (string) Email Body
- `$data` (string) Email Send Data

**Usage**

```php
add_filter('fluentform/email_summary_body', function ($emailBody, $data) {
    // Do your stuff here
    
    return $emailBody;
}, 10, 2);

```

**Reference**

`apply_filters('fluentform/email_summary_body', $emailBody, $data);`

This filter is located in FluentForm\App\Services\Scheduler\Scheduler -> processEmailReport()

</explain-block>

<explain-block title="fluentform/email_summary_subject">

You can use this filter to modify email subject.

**Parameters**

- `$emailSubject` (string) Email Subject

**Usage**

```php
add_filter('fluentform/email_summary_subject', function ($$emailSubject) {
    // Do your stuff here
    
    return $emailSubject;
}, 10, 1);

```

**Reference**

`apply_filters('fluentform/email_summary_subject', $emailSubject);`

This filter is located in FluentForm\App\Services\Scheduler\Scheduler -> processEmailReport()

</explain-block>

<explain-block title="fluentform/email_summary_body_text">

You can use this filter to modify email summary body.

**Parameters**

- `$generateText` (string) Email Summary Body
- `$submissions` (array) All Submissions

**Usage**

```php
add_filter('fluentform/email_summary_body_text', function ($generateText, $submissions) {
    // Do your stuff here
    
    return $generateText;
}, 10, 2);

```

**Reference**

`apply_filters('fluentform/email_summary_body_text', $generateText, $submissions);`

This filter is located in FluentForm\app\views\email\report\body.php

</explain-block>

<explain-block title="fluentform/email_summary_footer_text">

You can use this filter to modify email summary footer.

**Parameters**

- `$footerText` (string) Email Summary Footer

**Usage**

```php
add_filter('fluentform/email_summary_footer_text', function ($footerText) {
    // Do your stuff here
    
    return $footerText;
}, 10, 1);

```

**Reference**

`apply_filters('fluentform/email_summary_footer_text', $footerText);`

This filter is located in FluentForm\app\views\email\report\body.php

</explain-block>

<explain-block title="fluentform/email_template_footer_credit">

You can use this filter to modify email template footer credit text.

**Parameters**

- `$poweredBy` (string) Credit Text By Default Powered by FluentForm
- `$form` (object) Form Object
- `$notification` (array) Email Notification

**Usage**

```php
add_filter('fluentform/email_template_footer_credit', function ($poweredBy, $form, $notification) {
    // Do your stuff here
    
    return $footerText;
}, 10, 1);

```

**Reference**

`apply_filters('fluentform/email_template_footer_credit', $poweredBy, $form, $notification);`

This filter is located in FluentForm\app\views\email\template\footer.php

</explain-block>

<explain-block title="fluentform/email_template_email_heading">

You can use this filter to toggle email template header.

**Parameters**

- `$status` (boolean) Whether the email heading is enabled
- `$form` (object) Form Object
- `$notification` (array) Email Notification

**Usage**

```php
add_filter('fluentform/email_template_email_heading', function ($status, $form, $notification) {
    // Do your stuff here
    
    return $status;
}, 10, 3);

```

**Reference**

`apply_filters('fluentform/email_template_email_heading', false, $form, $notification);`

This filter is located in FluentForm\app\views\email\template\header.php

</explain-block>

<explain-block title="fluentform/email_template_header_image">

You can use this filter to toggle email header image.

**Parameters**

- `$status` (boolean) Whether the email header image is enabled
- `$form` (object) Form Object
- `$notification` (array) Email Notification

**Usage**

```php
add_filter('fluentform/email_template_header_image', function ($status, $form, $notification) {
    // Do your stuff here
    
    return $status;
}, 10, 3);

```

**Reference**

`apply_filters('fluentform/email_template_header_image', false, $form, $notification);`

This filter is located in FluentForm\app\views\email\template\header.php

</explain-block>

<explain-block title="fluentform/email_content_type_header">

You can use this filter to add email content type to header.

**Parameters**

- `$contentType` (string) Email Header Content Type By Default, text/html; charset=UTF-8

**Usage**

```php
add_filter('fluentform/email_content_type_header', function ($contentType) {
    // Do your stuff here
    
    return $contentType;
}, 10, 1);

```

**Reference**

`apply_filters('fluentform/email_content_type_header', false, $form, $notification);`

This filter is located in FluentForm\app\views\email\template\header.php

</explain-block>

<explain-block title="fluentform/email_template_colors">

You can use this filter to modify email template colors.

**Parameters**

- `$colors` (array) Colors

**Usage**

```php
add_filter('fluentform/email_template_colors', function ($colors) {
    // Do your stuff here
    
    return $colors;
}, 10, 1);

```

```php 
$colors = array(
    'background_color'      => '#f6f6f6',
    'body_background_color' => '#ffffff',
    'base_color'            => '#444444',
    'text_color'            => '#444444'
);
```

**Reference**

`apply_filters('fluentform/email_template_colors', $colors);`

This filter is located in FluentForm\app\views\email\template\styles.php

</explain-block>

<explain-block title="fluentform/email_form_resume_link_config">

You can change form resume link for partial submission of forms by using this filter.

**Parameters**

- `$emailFormat` (array) Email Format
- `$submittedData` (array) Partial Submitted Data
- `$requestData` (array) Request Data
- `$form` (object) Form

**Usage**

```php
add_filter('fluentform/email_form_resume_link_config', function ($emailFormat, $submittedData, $requestData, $form) {
    // Do your stuff here
    
    return $emailFormat;
}, 10, 4);

```

**Reference**

`apply_filters('fluentform/email_form_resume_link_config', $emailFormat, $submittedData, $requestData, $form));`

This filter is located in FluentFormPro\src\classes\DraftSubmissionsManager -> emailProgressLink()

</explain-block>

<explain-block title="fluentform/email_resume_link_response">

You can modify email resume link confirmation message by using this filter.

**Parameters**

- `$message` (string) Email Confirmation Message

**Usage**

```php
add_filter('fluentform/email_resume_link_response', function ($message) {
    // Do your stuff here
    
    return $message;
}, 10, 1);

```

**Reference**

`apply_filters('fluentform/email_resume_link_response', $message);`

This filter is located in FluentFormPro\src\classes\DraftSubmissionsManager -> emailProgressLink()

</explain-block>

<explain-block title="fluentform/email_resume_link_body">

You can modify email body of resume link for partial submission by using this filter.

**Parameters**

- `$emailBody` (string) Email Body
- `$form` (object) Form Object
- `$link` (string) Email Resume Link

**Usage**

```php
add_filter('fluentform/email_resume_link_body', function ($emailBody, $form, $link) {
    // Do your stuff here
    
    return $emailBody;
}, 10, 3);

```

**Reference**

`apply_filters('fluentform/email_resume_link_body', $emailBody, $form, $link);`

This filter is located in FluentFormPro\src\classes\DraftSubmissionsManager -> processEmail($settings, $form, $link, $toEmail)

</explain-block>

<explain-block title="fluentform/failed_integration_notify_email_data">

You can modify failed integration email notification by using this filter.

**Parameters**

- `$data` (array) Failed Integration Email Notification

**Usage**

```php
add_filter('fluentform/failed_integration_notify_email_data', function ($data) {
    // Do your stuff here
    
    return $data;
}, 10, 1);

```

**Reference**

`apply_filters('fluentform/failed_integration_notify_email_data', $data);`

This filter is located in FluentFormPro\src\classes\FailedIntegrationNotification -> broadCast($data)

</explain-block>

<explain-block title="fluentform/email_attachments">

You can modify email attachments by using this filter.

**Parameters**

- `$attachments` (array) Email Attachment
- `$processedValues` (array) Shortcode Parsed Value
- `$formData` (array) Form Data
- `$entry` (array) Submission Data
- `$form` (object) Form Object

**Usage**

```php
add_filter('fluentform/email_attachments', function ($attachments, $processedValues, $formData, $entry, $form) {
    // Do your stuff here
    
    return $attachments;
}, 10, 5);

```

**Reference**

`apply_filters('fluentform/email_attachments', $attachments, $processedValues, $formData, $entry, $form);`

This filter is located in FluentFormPro\src\classes\ResendNotificationHandler -> resendEntryEmail($entryId, $feed, $sendToType, $customRecipient, $form)

</explain-block>