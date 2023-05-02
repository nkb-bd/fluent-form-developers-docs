<explain-block title="fluentform/file_upload_options">

You can change Fluent Forms default file upload location by using this filter.

**Parameters**

- `$locations` (array) File Upload Location

**Usage**

```php
add_filter('fluentform/file_upload_options', function ($locations){

   // Do your stuff here
}, 10, 1);
```

**Reference**

`apply_filters('fluentform/file_upload_options', $locations);`

This filter is located in FluentForm\App\Helpers\Helper -> fileUploadLocations()

</explain-block>

<explain-block title="fluentform/skip_no_conflict">

You can toggle the no conflict mode using this filter.

**Parameters**

- `$isConflict` (boolean) Whether no conflict mode is enabled

**Usage**

```php
add_filter('fluentform/skip_no_conflict', function ($isSkip) {
   // Do your stuff here
   
   return $isSkip;
}, 10, 1);

```

**Reference**

`apply_filters('fluentform/skip_no_conflict', $isSkip);`

This filter is located in FluentForm\App\Hooks\actions.php

</explain-block>

<explain-block title="fluentform/permission_set">

You can add or modify Fluentform Permission Set using this filter.

**Parameters**

- `$permissionSet` (array) Permission set

**Usage**

```php
add_filter('fluentform/permission_set', function ($permissionSet) {
   // Do your stuff here
   
   array_push($permissionSet, 'fluentform_dashboard_access');
   return $permissionSet;
}, 10, 1);

```

**Reference**

`apply_filters('fluentform/permission_set', $data);`

This filter is located in FluentForm\App\Modules\Acl -> getPermissionSet()

</explain-block>

<explain-block title="'fluentform/verify_user_permission_' . $permission">

This filter verifies each permission.

**Parameters**

- `$allowed` (array) Form default Settings
- `$formId` (int) Form ID

**Usage**

```php
add_filter('fluentform/verify_user_permission_' . $permission, function ($allowed, $formId) {
   // Do your stuff here

   return $allowed;
}, 10, 2);

```

**Reference**

`apply_filters('fluentform/verify_user_permission_' . $permission, $allowed, $formId);`

This filter is located in FluentForm\App\Modules\Acl -> hasPermission($permissions, $formId = false)

</explain-block>

<explain-block title="fluentform/current_user_capability">

You can modify Current User Capability using this filter.

**Parameters**

- `$capability` (array) User Capabilities

**Usage**

```php
add_filter('fluentform/current_user_capability', function ($capability) {
   // Do your stuff here

   return $capability;
}, 10, 1);

```

**Reference**

`apply_filters('fluentform/current_user_capability', static::$capability);`

This filter is located in FluentForm\App\Modules\Acl -> getCurrentUserCapability()

</explain-block>

<explain-block title="fluentform/current_user_permissions">

You can modify Current User Permission using this filter.

**Parameters**

- `$userPermissions` (array) Current User Permissions

**Usage**

```php
add_filter('fluentform/current_user_permissions', function ($userPermissions) {
   // Do your stuff here

   return $userPermissions;
}, 10, 1);

```

**Reference**

`apply_filters('fluentform/current_user_permissions', $userPermissions);`

This filter is located in FluentForm\App\Models\Form -> getUserPermissions($user = false)

</explain-block>

<explain-block title="fluentform/nonce_error">

You can modify NONCE error message using this filter.

**Parameters**

- `$errorMessage` (string) Error Message

**Usage**

```php
add_filter('fluentform/nonce_error', function ($errorMessage) {
   // Do your stuff here

   return $errorMessage;
}, 10, 1);

```

**Reference**

`apply_filters('fluentform/nonce_error', $message);`

This filter is located in FluentForm\App\Services\Form\FormValidationService -> validateNonce()

</explain-block>

<explain-block title="fluentform/shortcode_defaults">

This filter sets the defaults values for the shortcode.

**Parameters**

- `$defaults` (array) Default Shortcode Values
- `$atts` (array) Shortcode Attributes

**Usage**

```php
add_filter('fluentform/shortcode_defaults', function($defaults , $atts) {
   // Do your stuff here

   return $atts;
}, 10, 2);

```

**Reference**

`apply_filters('fluentform/shortcode_defaults', $data, $atts);`

This filter is located in FluentForm\App\Modules\Component\Component -> addFluentFormShortCode()

</explain-block>

<explain-block title="fluentform/shortcode_feed_text">

This filter returns the message of the shortcode for a feed.

**Parameters**

- `$feedText` (string) Shortcode Feed Text
- `$form` (object) Form Object

**Usage**

```php
add_filter('fluentform/shortcode_feed_text', function ($feedText, $form) {
   // Do your stuff here

   return $feedText;
}, 10, 1);

```

**Reference**

`apply_filters('fluentform/shortcode_feed_text', $feedText, $form);`

This filter is located in FluentForm\App\Modules\Component\Component -> renderForm($atts)

</explain-block>

<explain-block title="fluentform/shortcode_feed_text">

This filter returns the input labels for the entries on the entries page.

**Parameters**

- `$stepText` (string) Active Step Text

**Usage**

```php
add_filter('fluentform/step_string', function ($stepText) {
   // Do your stuff here

   return $stepText;
}, 10, 1);

```

**Reference**

`apply_filters('fluentform/step_string', $stepText);`

This filter is located in FluentForm\App\Modules\Component\Component -> renderForm($atts)

</explain-block>

<explain-block title="fluentform/parse_default_value">

You can modify form default shortcode value using this filter.

**Parameters**

- `$value` (string) Parseable Shortcode Value
- `$form` (object) Form Object

**Usage**

```php
add_filter('fluentform/parse_default_value', function($value, $form) {
   // Do your stuff here

   return $value;
}, 10, 2);

```

**Reference**

`apply_filters('fluentform/parse_default_value', $attrDefaultValues[$pattern], $form);`

This filter is located in FluentForm\App\Modules\Component\Component -> replaceEditorSmartCodes($output, $form)


</explain-block>

<explain-block title="fluentform/parse_default_values">

You can modify Shortcode's all parseable values using this filter.

**Parameters**

- `$attrDefaultValues` (array) Parseable All Shortcode Values

**Usage**

```php
add_filter('fluentform/parse_default_values', function($attrDefaultValues) {
   // Do your stuff here

   return $attrDefaultValues;
}, 10, 1);

```

**Reference**

`apply_filters('fluentform/parse_default_values', $attrDefaultValues);`

This filter is located in FluentForm\App\Modules\Component\Component -> replaceEditorSmartCodes($output, $form)

</explain-block>

<explain-block title="fluentform/akismet_fields">

This filter is used in the Akismet handler.

**Parameters**

- `$info` (array) Akismet Data
- `$data` (array) Form Data
- `$form` (object) Form Object

**Usage**

```php
add_filter('fluentform/akismet_fields', function ($info, $data, $form) {
   // Do your stuff here

   return $info;
}, 10, 3);

```

**Reference**

`apply_filters('fluentform/akismet_fields', $info, $data, $form);`

This filter is located in FluentForm\App\Modules\AkismetHandler -> getAkismetFields($data, $form)

</explain-block>

<explain-block title="fluentform/find_shortcode_params">

This filter returns Fluent Forms shortcode used in the site.

**Parameters**

- `$params` (array) Post Type

**Usage**

```php
add_filter('fluentform/find_shortcode_params', function($params) {
   // Do your stuff here

   return $params;
}, 10, 1);

```

**Reference**

`apply_filters('fluentform/find_shortcode_params', $params);`

This filter is located in FluentForm\App\Services\Form\FormService -> findShortCodePage($formId)

</explain-block>

<explain-block title="fluentform/will_parse_url_value">

You can toggle redirect URL parsing in confirmation Message using the filter.

**Parameters**

- `$status` (boolean) Whether Parse the URL
- `$form` (object) Form Object

**Usage**

```php
add_filter('fluentform/will_parse_url_value', function($status, $form) {
   // Do your stuff here

   return $status;
}, 10, 2);

```

**Reference**

`apply_filters('fluentform/will_parse_url_value', $parseUrl, $form);`

This filter is located in FluentForm\App\Services\Form\SubmissionHandlerServices -> getReturnData($insertId, $form,
$formData)

</explain-block>

<explain-block title="fluentform/akismet_check_spam">

You can toggle Akismet spam checking using this filter.

**Parameters**

- `$status` (boolean) Whether Spam Check is enabled
- `$formId` (int) Form ID
- `$formData` (array) Form Data

**Usage**

```php
add_filter('fluentform/akismet_check_spam', function($status, $formId, $formData) {
   // Do your stuff here

   return $status;
}, 10, 3);

```

**Reference**

`apply_filters('fluentform/akismet_check_spam', $isSpamCheck, $form->id, $formData);`

This filter is located in FluentForm\App\Services\Form\FormValidationService -> isSpam($formData, $form)

</explain-block>

<explain-block title="fluentform/akismet_spam_result">

You can toggle Akismet spam result using this filter.

**Parameters**

- `$isSpam` (boolean) Whether Spam Check is enabled
- `$formId` (int) Form ID
- `$formData` (array) Form Data

**Usage**

```php
add_filter('fluentform/akismet_spam_result', function($isSpam, $formId, $formData) {
   // Do your stuff here

   return $defaultSettings;
}, 10, 1);

```

**Reference**

`apply_filters('fluentform/akismet_spam_result', $isSpam, $form->id, $formData);`

This filter is located in FluentForm\App\Services\Form\FormValidationService -> isSpam($formData, $form)

</explain-block>

<explain-block title="fluentform/has_recaptcha">

You can toggle Recaptcha using this filter.

**Parameters**

- `$status` (boolean) Whether Recaptcha is enabled

**Usage**

```php
add_filter('fluentform/has_recaptcha', function($status) {
   // Do your stuff here

   return $status;
}, 10, 1);

```

**Reference**

`apply_filters('fluentform/has_recaptcha', $hasAutoRecap);`

This filter is located in FluentForm\App\Services\Form\FormValidationService -> validateReCaptcha()

</explain-block>

<explain-block title="fluentform/has_hcaptcha">

You can toggle Hcaptcha using this filter.

**Parameters**

- `$status` (boolean) Whether Hcaptcha is enabled

**Usage**

```php
add_filter('fluentform/has_hcaptcha', function($status) {
   // Do your stuff here

   return $status;
}, 10, 1);

```

**Reference**

`apply_filters('fluentform/has_hcaptcha', $hasAutoHcap);`

This filter is located in FluentForm\App\Services\Form\FormValidationService -> validateHCaptcha()

</explain-block>

<explain-block title="fluentform/has_turnstile">

You can toggle Turnstile using this filter.

**Parameters**

- `$status` (boolean) Whether Turnstile is enabled

**Usage**

```php
add_filter('fluentform/has_turnstile', function($status) {
   // Do your stuff here

   return $status;
}, 10, 1);

```

**Reference**

`apply_filters('fluentform/has_turnstile', $hasAutoTurnsTile);`

This filter is located in FluentForm\App\Services\Form\FormValidationService -> validateTurnstile()

</explain-block>

<explain-block title="fluentform/recaptcha_v3_ref_score">

You can set Recaptcha Reference Score using this filter. By default, score is set to 0.5.

**Parameters**

- `$score` Reference Score between 0 and 1

**Usage**

```php
add_filter('fluentform/recaptcha_v3_ref_score', function($score) {
   // Do your stuff here

   return $score;
}, 10, 1);

```

**Reference**

`apply_filters('fluentforms/recaptcha_v3_ref_score', $value);`

This filter is located in FluentForm\App\Modules\ReCaptcha\ReCaptcha -> validate($token, $secret = null, $version = '
v2_visible')

</explain-block>

<explain-block title="'fluentform/editor_shortcode_callback_group_' . $group">

You can modify shortcode group using the filter.

**Parameters**

- `$handler` (array) All Shortcode Group
- `$form` (object) Form Object
- `$handlerArray` (array) Shortcode Handlers Group

**Usage**

```php
add_filter('fluentform/editor_shortcode_callback_group_' . $group, function ($handler, $form, $handlerArray) {
   // Do your stuff here

   return '{' . $handler . '}';
}, 10, 3);

```

**Reference**

`apply_filters('fluentform/editor_shortcode_callback_group_' . $group, '{' . $handler . '}', $form, $handlerArray);`

This filter is located in FluentForm\App\Services\FormBuilder\EditorShortcodeParser -> filter($value, $form)

</explain-block>

<explain-block title="'fluentform/editor_shortcode_callback_' . $handler">

You can modify shortcode handler using the filter.

**Parameters**

- `$handler` (array) Shortcode Handler Array
- `$form` (object) Form Object

**Usage**

```php
add_filter('fluentform/editor_shortcode_callback_' . $handler, function ($handler, $form) {
   // Do your stuff here

   return $handler;
}, 10, 2);

```

**Reference**

`apply_filters('fluentform/editor_shortcode_callback_' . $handler, $handler, $form);`

This filter is located in FluentForm\App\Services\FormBuilder\EditorShortcodeParser -> filter($value, $form)

</explain-block>

<explain-block title="fluentform/editor_element_customization_settings">

This filter returns the input element settings components in editor.

**Parameters**

- `$settings` (array) Element settings

**Usage**

```php
add_filter('fluentform/editor_element_customization_settings', function ($settings) {
    if ($customSettings = $this->getEditorCustomizationSettings()) {
    $settings = array_merge($settings, $customSettings);
    }

    return $settings;
}, 10, 1);

```

**Reference**

`apply_filters('fluentform/editor_element_customization_settings', $element_customization_settings);`

This filter is located in FluentForm\App\Services\FormBuilder\ElementCustomization

</explain-block>

<explain-block title="fluentform/html_attributes">

You can use this filter to modify the form attributes before form render.

**Parameters**

- `$data` (array) Form HTML attributes
- `$form` (object) Form Object

**Usage**

```php
add_filter('fluentform/html_attributes', function ($data, $form) {
    // Do your stuff here
    
    return $data;
}, 10, 2);

```

**Reference**

`apply_filters('fluentform/html_attributes', $data, $form);`

This filter is located in FluentForm\App\Services\FormBuilder\FormBuilder -> build($form, $extraCssClass = '',
$instanceCssClass = '', $atts = [])

</explain-block>

<explain-block title="fluentform/all_data_skip_password_field">

You can use this filter to skip password for {all_data} shortcode.

**Parameters**

- `$status` (boolean) Whether to skip the password field

**Usage**

```php
add_filter('fluentform/all_data_skip_password_field', function ($status) {
    // Do your stuff here
    
    return $status;
}, 10, 1);

```

**Reference**

`apply_filters('fluentform/all_data_skip_password_field',  __return_true());`

This filter is located in FluentForm\App\Services\FormBuilder\ShortcodeParser -> getOtherData($key)

</explain-block>

<explain-block title="fluentform/all_data_without_hidden_fields">

You can use this filter to skip hidden field for {all_data} shortcode.

**Parameters**

- `$status` (boolean) Whether to skip the hidden field

**Usage**

```php
add_filter('fluentform/all_data_without_hidden_fields', function ($status) {
    // Do your stuff here
    
    return $status;
}, 10, 1);

```

**Reference**

`apply_filters('fluentform/all_data_without_hidden_fields',  __return_true());`

This filter is located in FluentForm\App\Services\FormBuilder\ShortcodeParser -> getOtherData($key)

</explain-block>

<explain-block title="fluentform/all_data_shortcode_html">

You can use this filter to modify {all_data} shortcode as HTML.

**Parameters**

- `$html` (string) HTML string
- `$formFields` (array) Form Fields
- `$inputLabels` (array) Input Labels
- `$response` (object) Form Response

**Usage**

```php
add_filter('fluentform/all_data_shortcode_html', function ($html, $formFields, $inputLabels, $response) {
    // Do your stuff here
    
    return $html;
}, 10, 1);

```

**Reference**

`apply_filters('fluentform/all_data_shortcode_html',  __return_true());`

This filter is located in FluentForm\App\Services\FormBuilder\ShortcodeParser -> getOtherData($key)

</explain-block>

<explain-block title="fluentform/shortcode_parser_callback_pdf.download_link.public">

You can use this filter to modify the public PDF download link.

**Parameters**

- `$key` (string) Key Name
- `$instance` (object) Shortcode Parser Instance

**Usage**

```php
add_filter('fluentform/shortcode_parser_callback_pdf.download_link.public', function ($key, $instance) {
    // Do your stuff here
    
    return $key;
}, 10, 2);

```

**Reference**

`apply_filters('fluentform/shortcode_parser_callback_pdf.download_link.public', $key, $instance);`

This filter is located in FluentForm\App\Services\FormBuilder -> getOtherData($key)

</explain-block>

<explain-block title="fluentform/shortcode_parser_callback_random_string">

You can use this filter to modify the any shortcode with random string.

**Parameters**

- `$value` (string) Name of the Shortcode after .
- `$prefix` (string) Prefix of the Shortcode before .
- `$instance` (object) Shortcode Parser Instance

**Usage**

```php
add_filter('fluentform/shortcode_parser_callback_random_string', function ($value, $prefix, $instance) {
    // Do your stuff here
    
    return $value;
}, 10, 3);

```

**Reference**

`apply_filters('fluentform/shortcode_parser_callback_random_string', $value, $prefix, static::getInstance());`

This filter is located in FluentForm\App\Services\FormBuilder -> getOtherData($key)

</explain-block>

<explain-block title="'fluentform/smartcode_group_' . $group">

You can use this filter to modify the smartcode with a specific group.

**Parameters**

- `$property` (string) Smartcode Name
- `$instance` (object) Shortcode Parser Instance

**Usage**

```php
add_filter('fluentform/smartcode_group_' . $group, function ($property, $instance) {
    // Do your stuff here
    
    return $value;
}, 10, 2);

```

**Reference**

`apply_filters('fluentform/smartcode_group_' . $group, $property, static::getInstance());`

This filter is located in FluentForm\App\Services\FormBuilder -> getOtherData($key)

</explain-block>

<explain-block title="'fluentform/shortcode_parser_callback_' . $key">

You can use this filter to modify the any shortcode with matching key.

**Parameters**

- `$key` (string) Key Name
- `$instance` (object) Shortcode Parser Instance

**Usage**

```php
add_filter('fluentform/shortcode_parser_callback_' . $key, function ($key, $instance) {
    // Do your stuff here
    
    return $key;
}, 10, 3);

```

**Reference**

`apply_filters('fluentform/shortcode_parser_callback_' . $key, static::getInstance());`

This filter is located in FluentForm\App\Services\FormBuilder -> getOtherData($key)

</explain-block>

<explain-block title="fluentform/editor_validation_rule_settings">

You can modify validation rule for any input using the filter.

**Parameters**

- `$validation_rule_settings` (array) Validation Rule Settings for all input

**Usage**

```php
add_filter('fluentform/editor_validation_rule_settings', function ($validation_rule_settings) {
    // Do your stuff here
    
    return $validation_rule_settings;
}, 10, 1);

```

```php
$validation_rule_settings = [
    'required' => [
        'template'  => 'inputRadio',
        'label'     => __('Required', 'fluentform'),
        'help_text' => __('Select whether this field is a required field for the form or not.', 'fluentform'),
        'options'   => [
            [
                'value' => true,
                'label' => __('Yes', 'fluentform'),
            ],
            [
                'value' => false,
                'label' => __('No', 'fluentform'),
            ],
        ],
    ],
    'valid_phone_number' => [
        'template'  => 'inputRadio',
        'label'     => __('Validate Phone Number', 'fluentform'),
        'help_text' => __('Select whether the phone number should be validated or not.', 'fluentform'),
        'options'   => [
            [
                'value' => true,
                'label' => __('Yes', 'fluentform'),
            ],
            [
                'value' => false,
                'label' => __('No', 'fluentform'),
            ],
        ],
    ],
    'email' => [
        'template'  => 'inputRadio',
        'label'     => __('Validate Email', 'fluentform'),
        'help_text' => __('Select whether to validate this field as email or not', 'fluentform'),
        'options'   => [
            [
                'value' => true,
                'label' => __('Yes', 'fluentform'),
            ],
            [
                'value' => false,
                'label' => __('No', 'fluentform'),
            ],
        ],
    ],
    'url' => [
        'template'  => 'inputRadio',
        'label'     => __('Validate URL', 'fluentform'),
        'help_text' => __('Select whether to validate this field as URL or not', 'fluentform'),
        'options'   => [
            [
                'value' => true,
                'label' => __('Yes', 'fluentform'),
            ],
            [
                'value' => false,
                'label' => __('No', 'fluentform'),
            ],
        ],
    ],
    'min' => [
        'template'  => 'inputText',
        'type'      => 'number',
        'label'     => __('Min Value', 'fluentform'),
        'help_text' => __('Minimum value for the input field.', 'fluentform'),
    ],
    'digits' => [
        'template'  => 'inputText',
        'type'      => 'number',
        'label'     => __('Digits', 'fluentform'),
        'help_text' => __('Number of digits for the input field.', 'fluentform'),
    ],
    'max' => [
        'template'  => 'inputText',
        'type'      => 'number',
        'label'     => __('Max Value', 'fluentform'),
        'help_text' => __('Maximum value for the input field.', 'fluentform'),
    ],
    'max_file_size' => [
        'template'  => 'maxFileSize',
        'label'     => __('Max File Size', 'fluentform'),
        'help_text' => __('The file size limit uploaded by the user.', 'fluentform'),
    ],
    'max_file_count' => [
        'template'  => 'inputText',
        'type'      => 'number',
        'label'     => __('Max Files Count', 'fluentform'),
        'help_text' => __('Maximum user file upload number.', 'fluentform'),
    ],
    'allowed_file_types' => [
        'template'  => 'inputCheckbox',
        'label'     => __('Allowed Files', 'fluentform'),
        'help_text' => __('Allowed Files', 'fluentform'),
        'fileTypes' => [
            [
                'title' => __('Images', 'fluentform'),
                'types' => ['jpg', 'jpeg', 'gif', 'png', 'bmp'],
            ],
            [
                'title' => __('Audio', 'fluentform'),
                'types' => ['mp3', 'wav', 'ogg', 'oga', 'wma', 'mka', 'm4a', 'ra', 'mid', 'midi'],
            ],
            [
                'title' => __('Video', 'fluentform'),
                'types' => [
                    'avi',
                    'divx',
                    'flv',
                    'mov',
                    'ogv',
                    'mkv',
                    'mp4',
                    'm4v',
                    'divx',
                    'mpg',
                    'mpeg',
                    'mpe',
                ],
            ],
            [
                'title' => __('PDF', 'fluentform'),
                'types' => ['pdf'],
            ],
            [
                'title' => __('Docs', 'fluentform'),
                'types' => [
                    'doc',
                    'ppt',
                    'pps',
                    'xls',
                    'mdb',
                    'docx',
                    'xlsx',
                    'pptx',
                    'odt',
                    'odp',
                    'ods',
                    'odg',
                    'odc',
                    'odb',
                    'odf',
                    'rtf',
                    'txt',
                ],
            ],
            [
                'title' => __('Zip Archives', 'fluentform'),
                'types' => ['zip', 'gz', 'gzip', 'rar', '7z', ],
            ],
            [
                'title' => __('Executable Files', 'fluentform'),
                'types' => ['exe'],
            ],
            [
                'title' => __('CSV', 'fluentform'),
                'types' => ['csv'],
            ],
        ],
        'options' => $fileTypeOptions,
    ],
    'allowed_image_types' => [
        'template'  => 'inputCheckbox',
        'label'     => __('Allowed Images', 'fluentform'),
        'help_text' => __('Allowed Images', 'fluentform'),
        'fileTypes' => [
            [
                'title' => __('JPG', 'fluentform'),
                'types' => ['jpg|jpeg', ],
            ],
            [
                'title' => __('PNG', 'fluentform'),
                'types' => ['png'],
            ],
            [
                'title' => __('GIF', 'fluentform'),
                'types' => ['gif'],
            ],
        ],
        'options' => [
            [
                'label' => __('JPG', 'fluentform'),
                'value' => 'jpg|jpeg',
            ],
            [
                'label' => __('PNG', 'fluentform'),
                'value' => 'png',
            ],
            [
                'label' => __('GIF', 'fluentform'),
                'value' => 'gif',
            ],
        ],
    ],
];

```

**Reference**

`apply_filters('fluentform/editor_validation_rule_settings', $validation_rule_settings);`

This filter is located in FluentForm\App\Services\FormBuilder\ValidationRuleSettings

</explain-block>

<explain-block title="fluentform/cleanup_days_count">

You can use this filter to set days count for cleanup old data through scheduler.

**Parameters**

- `$days` (int) Days Count, By default 60

**Usage**

```php
add_filter('fluentform/cleanup_days_count', function ($days) {
    // Do your stuff here
    
    return $days;
}, 10, 1);

```

**Reference**

`apply_filters('fluentform/cleanup_days_count', $days);`

This filter is located in FluentForm\App\Services\Scheduler\Scheduler -> cleanUpOldData()

</explain-block>

<explain-block title="fluentform/allowed_html_tags">

You can use this filter to add HTML attributes for sanitization.

**Parameters**

- `$tags` (array) HTML Attributes

**Usage**

```php
add_filter('fluentform/allowed_html_tags', function ($tags) {
    // Do your stuff here
    
    return $tags;
}, 10, 1);

```

**Reference**

`apply_filters('fluentform/allowed_html_tags', $tags);`

This filter is located in FluentForm\boot\globals.php -> fluentform_sanitize_html($html)

</explain-block>

<explain-block title="fluentform/backend_sanitized_values">

You can use this filter to add inputs values for sanitization.

**Parameters**

- `$inputs` (array) Form Inputs

**Usage**

```php
add_filter('fluentform/backend_sanitized_values', function ($inputs) {
    // Do your stuff here
    
    return $inputs;
}, 10, 1);

```

**Reference**

`apply_filters('fluentform/backend_sanitized_values', $inputs);`

This filter is located in FluentForm\boot\globals.php -> fluentform_backend_sanitizer($inputs, $sanitizeMap = [])

</explain-block>

<explain-block title="fluentform/disable_fields_sanitize">

You can use this filter to toggle disable fields sanitization.

**Parameters**

- `$status` (boolean) Whether disabled fields sanitization is enabled

**Usage**

```php
add_filter('fluentform/disable_fields_sanitize', function ($status) {
    // Do your stuff here
    
    return $status;
}, 10, 1);

```

**Reference**

`apply_filters('fluentform/disable_fields_sanitize', $status);`

This filter is located in FluentForm\boot\globals.php -> fluentformCanUnfilteredHTML()

</explain-block>

<explain-block title="fluentform/disabled_components">

You can use this filter to modify disabled components.

**Parameters**

- `$disabled` (array) Disabled Components

**Usage**

```php
add_filter('fluentform/disabled_components', function ($disabled) {
    // Do your stuff here
    
    return $disabled;
}, 10, 1);

```

```php
$disabled['ratings'] = [
    'disabled'    => true,
    'title'       => __('Ratings', 'fluentform'),
    'description' => __('Ratings is not available with the free version. Please upgrade to pro to get all the advanced features.', 'fluentform'),
    'image'       => '',
    'video'       => 'https://www.youtube.com/embed/YGdkNspMaEs',
];
$disabled['tabular_grid'] = [
    'disabled'    => true,
    'title'       => __('Checkable Grid', 'fluentform'),
    'description' => __('Checkable Grid is not available with the free version. Please upgrade to pro to get all the advanced features.', 'fluentform'),
    'image'       => '',
    'video'       => 'https://www.youtube.com/embed/ayI3TzXXANA',
];
```

**Reference**

`apply_filters('fluentform/disabled_components', $disabled);`

This filter is located in FluentForm\app\Services\Form\FormServices -> getDisabledComponents()

</explain-block>

<explain-block title="fluentform/validation_error">

This filter hook is fired before form render. You can use this to change rendered form.

**Parameters**

- `$errors` (array) Validation Errors
- `$formData` (array) Form Data
- `$form` (object) Form Object
- `$fields` (array) Form Fields

**Usage**

```php
add_filter('fluentform/validation_error', function ($errors, $formData, $form, $fields) {
    // Do your stuff here
    
    return $returnData;
}, 10, 4);

```

**Reference**

`apply_filters('fluentform/validation_error', $errors, $this->form, $fields, $this->formData);`

This filter is located in FluentForm\app\Services\Form\SubmissionHandlerService -> getReturnData($insertId, $form,
$formData)

</explain-block>

<explain-block title="fluentform/nonce_verify">

You can use this to toggle the nonce verification of the rendered form.

**Parameters**

- `$status` (boolean) Whether the nonce verification is enabled
- `$formId` (int) Form ID

**Usage**

```php
add_filter('fluentform/nonce_verify', function ($status, $formId) {
    // Do your stuff here
    
    return $status;
}, 10, 2);

```

**Reference**

`apply_filters('fluentform/nonce_verify', false, $formId);`

This filter is located in FluentForm\app\Services\Form\FormValidationService -> validateNonce()

</explain-block>

<explain-block title="fluentform/https_local_ssl_verify">

You can use this to toggle the local SSL verification for async requests.

**Parameters**

- `$status` (boolean) Whether local SSL verification is enabled

**Usage**

```php
add_filter('fluentform/https_local_ssl_verify', function ($status) {
    // Do your stuff here
    
    return $status;
}, 10, 1);

```

**Reference**

`apply_filters('fluentform/https_local_ssl_verify', false);`

This filter is located in FluentForm\app\Services\WPAsync\FluentFormAsyncRequest -> dispatchAjax($data = [])

</explain-block>

<explain-block title="fluentform/submission_cards">

You can use this filter to modify submission page cards.

**Parameters**

- `$cards` (array) Submission Cards
- `$resources` (array) Submission Resources
- `$submission` (array) Submission

**Usage**

```php
add_filter('fluentform/submission_cards', function ($cards, $resources, $submission) {
    // Do your stuff here
    
    return $cards;
}, 10, 3);

```

**Reference**

`apply_filters('fluentform/submission_cards', $cards, $resources, $submission);`

This filter is located in Fluentform\app\services\Submission\SubmissionService -> resources($attributes)

</explain-block>

<explain-block title="fluentform/submission_order_data">

You can use this filter to toggle submission payment order.

**Parameters**

- `$order_data` (boolean) Whether submission payment order is available
- `$submission` (array) Submission
- `$form` (object) Form Object

**Usage**

```php
add_filter('fluentform/submission_order_data', function ($order_data, $submission, $form) {
    // Do your stuff here
    
    return $order_data;
}, 10, 3);

```

**Reference**

`apply_filters('fluentform/submission_order_data', $order_data, $submission, $form);`

This filter is located in Fluentform\app\services\Submission\SubmissionService -> _getEntry()

</explain-block>

<explain-block title="fluentform/auto_read">

You can use this filter to toggle submission status to read automatically.

**Parameters**

- `$autoRead` (boolean) Whether change submission status to read
- `$form` (object) Form Object

**Usage**

```php
add_filter('fluentform/auto_read', function ($autoRead, $form) {
    // Do your stuff here
    
    return $autoRead;
}, 10, 2);

```

**Reference**

`apply_filters('fluentform/auto_read', $autoRead, $form);`

This filter is located in Fluentform\app\Modules\Entries\Entries -> _getEntry()

</explain-block>

<explain-block title="fluentform/auto_read_submission">

You can use this filter to toggle submission status to read automatically.

**Parameters**

- `$autoRead` (boolean) Whether change submission status to read
- `$form` (object) Form Object

**Usage**

```php
add_filter('fluentform/auto_read_submission', function ($autoRead, $form) {
    // Do your stuff here
    
    return $autoRead;
}, 10, 2);

```

**Reference**

`apply_filters('fluentform/auto_read_submission', $autoRead, $form);`

This filter is located in Fluentform\app\Services\Submission\SubmissionService -> find($submissionId)

</explain-block>

<explain-block title="fluentform/submissions_widgets">

You can use this filter to modify submission widgets.

**Parameters**

- `$widgets` (array) Submission Widgets
- `$resources` (array) Submission Resources
- `$submission` (array) Submission

**Usage**

```php
add_filter('fluentform/submissions_widgets', function ($widgets, $resources, $submission) {
    // Do your stuff here
    
    return $widgets;
}, 10, 3);

```

**Reference**

`apply_filters('fluentform/submissions_widgets', $widgets, $resources, $submission);`

This filter is located in Fluentform\app\Services\Submission\SubmissionService -> resources($attributes)

</explain-block>

<explain-block title="fluentform/submission_resources">

You can use this filter to modify all submission resources.

**Parameters**

- `$resources` (array) Submission Resources

**Usage**

```php
add_filter('fluentform/submission_resources', function ($resources) {
    // Do your stuff here
    
    return $resources;
}, 10, 1);

```

**Reference**

`apply_filters('fluentform/submission_resources', $resources);`

This filter is located in Fluentform\app\Services\Submission\SubmissionService -> resources($attributes)

</explain-block>

<explain-block title="fluentform/inventory_fields_before_render">

You can use this filter to modify inventory form fields.

**Parameters**

- `$field` (array) Form Fields
- `$form` (object) Form Object
- `$previousSubmissionData` (array) Previous Form Submission

**Usage**

```php
add_filter('fluentform/inventory_fields_before_render', function ($field, $form, $previousSubmissionData) {
    // Do your stuff here
    
    return $field;
}, 10, 3);

```

**Reference**

`apply_filters('fluentform/inventory_fields_before_render', $field, $form, $previousSubmissionData);`

This filter is located in FluentFormPro\src\classes\Inventory\InventoryFieldsRenderer -> processInventoryFields($field,
$form, $previousSubmissionData)

</explain-block>

<explain-block title="fluentform/inventory_inputs">

You can use this filter to modify inventory input fields.

**Parameters**

- `$fields` (array) Inventory Input Fields

**Usage**

```php
add_filter('fluentform/inventory_inputs', function ($fields) {
    // Do your stuff here
    
    return $fields;
}, 10, 1);

```

```php
$fields = [
    'select',
    'input_radio',
    'input_checkbox',
    'multi_payment_component'
];
```

**Reference**

`apply_filters('fluentform/inventory_inputs', $fields);`

This filter is located in FluentFormPro\src\classes\Inventory\InventorySettingsManager -> getInventoryInputs()

</explain-block>

<explain-block title="fluentform/inventory_validation_error">

You can use this filter to modify inventory stock out error message.

**Parameters**

- `$stockOutMsg` (string) Error Message
- `$fieldName` (array) Inventory Fields
- `$item` (array) Inventory Item
- `$formData` (array) Form Data
- `$form` (object) Form

**Usage**

```php
add_filter('fluentform/inventory_validation_error', function ($stockOutMsg, $fieldName, $item, $formData, $form) {
    // Do your stuff here
    
    return $stockOutMsg;
}, 10, 5);

```

**Reference**

`apply_filters('fluentform/inventory_validation_error', $stockOutMsg, $fieldName, $item, $this->formData, $this->form);`

This filter is located in FluentFormPro\src\classes\Inventory\InventoryValidation -> validate()

</explain-block>

<explain-block title="fluentform/conditional_shortcode_defaults">

You can use this filter to modify shortcode default.

**Parameters**

- `$default` (array) Shortcode Default
- `$atts` (array) Shortcode Attributes

**Usage**

```php
add_filter('fluentform/conditional_shortcode_defaults', function ($default, $atts) {
    // Do your stuff here
    
    return $default;
}, 10, 2);

```
```php
$default = [
    'field' => '',
    'is'    => '',
    'to'    => ''
];
```

**Reference**

`apply_filters('fluentform/conditional_shortcode_defaults', $default, $atts);`

This filter is located in FluentFormPro\src\classes\ConditionalContent -> handle($atts, $content)

</explain-block>

<explain-block title="fluentform/submission_vars">

You can modify submission variables on double optin confirmation by using this filter.

**Parameters**

- `$submissionVars` (array) Submission Variable
- `$formId` (int) Form ID

**Usage**

```php
add_filter('fluentform/submission_vars', function ($submissionVars, $formId) {
    // Do your stuff here
    
    return $submissionVars;
}, 10, 2);

```
```php
$submissionVars = [
    'settings'        => $settings,
    'title'           => 'Submission Confirmed - ' . $form->title,
    'form_id'         => $formId,
    'entry'           => $entry,
    'form'            => $form,
    'bg_color'        => $settings['custom_color'],
    'landing_content' => $message,
    'has_header'      => false,
    'isEmbeded'       => !!ArrayHelper::get($_GET, 'embedded')
];
```

**Reference**

`apply_filters('fluentform/submission_vars', $submissionVars, $formId);`

This filter is located in FluentFormPro\src\classes\DoubleOption -> confirmSubmission($data)

</explain-block>

<explain-block title="fluentform/disable_attachment_delete">

You can toggle double option confirmation file attachment by using this filter.

**Parameters**

- `$status` (boolean) Whether the attachment is disabled
- `$formId` (int) Form ID

**Usage**

```php
add_filter('fluentform/disable_attachment_delete', function ($status, $formId) {
    // Do your stuff here
    
    return $status;
}, 10, 2);

```

**Reference**

`apply_filters('fluentform/disable_attachment_delete', $status, $entry->form_id));`

This filter is located in FluentFormPro\src\classes\DoubleOption -> deleteAssociateFiles($entry)

</explain-block>

<explain-block title="fluentform/style_presets">

You can modify form styler by using this filter.

**Parameters**

- `$presets` (array) Form Styler Presets

**Usage**

```php
add_filter('fluentform/style_presets', function ($presets) {
    // Do your stuff here
    
    return $presets;
}, 10, 1);

```
```php
$presets = [
    '' => [
        'label' => __('Default', ''),
        'src' => ''
    ],
    'ffs_modern_b' => [
        'label' => __('Modern (Bold)', ''),
        'src' => FLUENTFORMPRO_DIR_URL . 'public/css/skin_modern_bold.css'
    ],
    'ffs_modern_l' => [
        'label' => __('Modern (Light)', ''),
        'src' => FLUENTFORMPRO_DIR_URL . 'public/css/skin_modern_light.css'
    ],
    'ffs_classic' => [
        'label' => __('Classic', ''),
        'src' => FLUENTFORMPRO_DIR_URL . 'public/css/skin_classic.css'
    ],
    'ffs_bootstrap' => [
        'label' => __('Bootstrap Style', ''),
        'src' => FLUENTFORMPRO_DIR_URL . 'public/css/skin_bootstrap.css'
    ],
];
```

**Reference**

`apply_filters('fluentform/style_presets', $presets);`

This filter is located in FluentFormPro\src\classes\FormStyler -> getPresets()

</explain-block>

<explain-block title="fluentform/step_form_entry_vars">

You can modify step form submission variables by using this filter.

**Parameters**

- `$entryVars` (array) Step Form Submission Variables
- `$form` (object) Form Object

**Usage**

```php
add_filter('fluentform/step_form_entry_vars', function ($entryVars, $form) {
    // Do your stuff here
    
    return $entryVars;
}, 10, 2);

```
```php
$entryVars = [
    'form_id' => $form->id,
    'current_form_title' => $form->title,
    'has_pro' => defined('FLUENTFORMPRO'),
    'all_forms_url' => admin_url('admin.php?page=fluent_forms'),
    'printStyles' => [fluentformMix('css/settings_global.css')],
    'entries_url_base' => admin_url('admin.php?page=fluent_forms&route=msformentries&form_id='),
    'available_countries' => getFluentFormCountryList(),
    'no_found_text' => __('Sorry! No entries found. All your entries will be shown here once you start getting form submissions', 'fluentformpro')
];
```

**Reference**

`apply_filters('fluentform/step_form_entry_vars', $entryVars, $form);`

This filter is located in FluentFormPro\src\classes\StepFormEntries -> renderEntries($form_id)

</explain-block>

<explain-block title="fluentform/all_entries">

You can modify all submissions using the filter.

**Parameters**

- `$submission` (array) Form Submission

**Usage**

```php
add_filter('fluentform/all_entries', function ($submission) {
    // Do your stuff here
    
    return $submission;
}, 10, 1);

```

**Reference**

`apply_filters('fluentform/all_entries', $entries['submissions']);`

This filter is located in FluentFormPro\src\classes\StepFormEntries -> getEntries()

</explain-block>

<explain-block title="fluentform/single_response_data">

You can modify submission of a certain form using this filter.

**Parameters**

- `$submission` (array) Form Submission
- `$formId` (int) Form ID

**Usage**

```php
add_filter('fluentform/single_response_data', function ($submission, $formId) {
    // Do your stuff here
    
    return $submission;
}, 10, 2);

```

**Reference**

`apply_filters('fluentform/single_response_data', $submission, $this->formId);`

This filter is located in FluentFormPro\src\classes\StepFormEntries -> getstepFormEntry()

</explain-block>

<explain-block title="fluentform/single_response_input_fields">

You can modify inputs of a submission under a certain form using this filter.

**Parameters**

- `$inputs` (array) Form Inputs
- `$formId` (int) Form ID

**Usage**

```php
add_filter('fluentform/single_response_input_fields', function ($inputs, $formId) {
    // Do your stuff here
    
    return $inputs;
}, 10, 2);

```

**Reference**

`apply_filters('fluentform/single_response_input_fields', $formMeta['inputs'], $this->formId);`

This filter is located in FluentFormPro\src\classes\StepFormEntries -> getstepFormEntry()

</explain-block>

<explain-block title="fluentform/single_response_input_labels">

You can modify input labels of a submission under a certain form using this filter.

**Parameters**

- `$labels` (array) Form Input Labels
- `$formId` (int) Form ID

**Usage**

```php
add_filter('fluentform/single_response_input_labels', function ($labels, $formId) {
    // Do your stuff here
    
    return $labels;
}, 10, 2);

```

**Reference**

`apply_filters('fluentform/single_response_input_labels', $formMeta['labels'], $this->formId);`

This filter is located in FluentFormPro\src\classes\StepFormEntries -> getstepFormEntry()

</explain-block>

<explain-block title="fluentform/post_type_selection_types_args">

You can modify post type args using this filter.

**Parameters**

- `$args` (array) Post Type Args

**Usage**

```php
add_filter('fluentform/post_type_selection_types_args', function ($args) {
    // Do your stuff here
    
    return $args;
}, 10, 1);

```

**Reference**

`apply_filters('fluentform/post_type_selection_types_args', $args);`

This filter is located in FluentFormPro\src\Components\PostSelectionField -> generalEditorElement()

</explain-block>

<explain-block title="fluentform/post_selection_types">

You can modify post selection types using this filter.

**Parameters**

- `$formattedTypes` (array) Post Selection Types

**Usage**

```php
add_filter('fluentform/post_selection_types', function ($formattedTypes) {
    // Do your stuff here
    
    return $formattedTypes;
}, 10, 1);

```

**Reference**

`apply_filters('fluentform/post_selection_types', $formattedTypes);`

This filter is located in FluentFormPro\src\Components\PostSelectionField -> generalEditorElement()

</explain-block>

<explain-block title="'fluentform/integration_data_' . $this->integrationKey">

You can modify any integration data through valid integration key before form submission by using this filter.

**Parameters**

- `$addData` (array) Submitted Data
- `$feed` (array) Form Feed
- `$entry` (array) Submission

**Usage**

```php
add_filter('fluentform/integration_data_' . $this->integrationKey, function ($addData, $feed, $entry) {
    // Do your stuff here
    
    return $addData;
}, 10, 3);

```

**Reference**

`apply_filters('fluentform/integration_data_' . $this->integrationKey, $addData, $feed, $entry);`

This filter is located in FluentFormPro\src\Integrations\ActiveCampaign\Bootstrap -> notify($feed, $formData, $entry, $form)

</explain-block>

<explain-block title="fluentform/integration_constantcontact_action_by">

You can edit constant contact API url action using the filter.

**Parameters**

- `$actionName` (array) Action Name

**Usage**

```php
add_filter('fluentform/integration_constantcontact_action_by', function ($actionName) {
    // Do your stuff here
    
    return $actionName;
}, 10, 1);

```

**Reference**

`apply_filters('fluentform/integration_constantcontact_action_by', $actionName);`

This filter is located in FluentFormPro\src\Integrations\ConstantContact\API -> getApiUrl($resource)

</explain-block>

<explain-block title="fluentform/hubspot_field_data">

You can modify hubspot feed field data before form submission using the filter.

**Parameters**

- `$fields` (array) Form Fields
- `$feed` (array) Hubspot Feed
- `$entry` (array) Submission
- `$form` (object) Form Object

**Usage**

```php
add_filter('fluentform/hubspot_field_data', function ($fields, $feed, $entry, $form) {
    // Do your stuff here
    
    return $fields;
}, 10, 4);

```

**Reference**

`apply_filters('fluentform/hubspot_field_data', $fields, $feed, $entry, $form);`

This filter is located in FluentFormPro\src\Integrations\Hubspot\Bootstrap -> notify($feed, $formData, $entry, $form)

</explain-block>

<explain-block title="fluentform/icontact_request_args">

You can modify IContact GET / POST Feed data using the filter.

**Parameters**

- `$options` (array) Feed Data
- `$action` (string) IContact API Action
- `$method` (string) GET/POST Method
- `$return_key` (string) Return Key

**Usage**

```php
add_filter('fluentform/icontact_request_args', function ($options, $action, $method, $return_key) {
    // Do your stuff here
    
    return $options;
}, 10, 4);

```

**Reference**

`apply_filters('fluentform/icontact_request_args', $options, $action, $method, $return_key);`

This filter is located in FluentFormPro\src\Integrations\IContact\IContactApi -> make_request( $action = null, $options = array(), $method = 'GET', $return_key = null )

</explain-block>

<explain-block title="fluentform/integration_discord_message">

You can modify discord message arguments using the filter.

**Parameters**

- `$messageArgs` (array) Discord Message Args
- `$feed` (array) Form Feed

**Usage**

```php
add_filter('fluentform/integration_discord_message', function ($messageArgs, $feed) {
    // Do your stuff here
    
    return $messageArgs; 
}, 10, 2);

```
```php
$messageArgs = [
    'embeds' => [
        0 => [
            'fields' => $fields,
            'title' => esc_html($messageTitle),
            'url' => esc_url_raw($entryLink),
            'description' => sanitize_text_field($description),
            'color' => hexdec('3F9EFF'),
            'footer' => [
                'text' => sanitize_text_field($footer)
            ]
        ],
    ],
    'content' => '*New submission on '. $form->title.' (#' . $entry->id . ')*'
];
```

**Reference**

`apply_filters('fluentform/integration_discord_message', $messageArgs, $feed);`

This filter is located in FluentFormPro\src\Integrations\Discord\Bootstrap -> notify($feed, $formData, $entry, $form)

</explain-block>
