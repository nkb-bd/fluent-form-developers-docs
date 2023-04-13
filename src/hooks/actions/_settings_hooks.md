
<explain-block title="fluentform/admin_nav_menu_{$item_key}">

**Description**

This action runs when add Fluent Forms admin menu

**Usage:**
```php 
add_action('fluentform/admin_nav_menu_{$item_key}', function() {
   // Do your stuff when add fluentform admin menu
}, 10, 0);
```

**Note:** `{$item_key}` is a dynamic key. Replace `{$item_key}` with Fluent Forms admin menu key.

**Reference**

`do_action("fluentform/admin_nav_menu_{$itemKey}");`

This action is located in `fluentform/app/Modules/Registerer/AdminBar.php`

</explain-block>

------------------------------------------------

<explain-block title="fluentform/after_save_form_settings">

**Description**

This action runs after saving the form from admin panel. You can hook into this action and extract any data you data need from the $allSettings array.

**Parameters**
- $formId (int) Form Id
- $allSettings (array) Form All Settings

**Usage:**
```php 
add_action('fluentform/after_save_form_settings', function($formId, $allSettings) {
   // Do your stuff when 
}, 10, 2);
```

**Reference**

`do_action('fluentform/after_save_form_settings', $formId, $attributes);`

This action is located in `fluentform/app/Services/Settings/SettingsService.php`, `fluentform/app/Modules/Form/Settings/FormSettings.php`

</explain-block>

------------------------------------------------

<explain-block title="fluentform/before_global_settings_wrapper">

**Description**

Before rendering the form global settings page this hook is available.

**Usage:**
```php 
add_action('fluentform/before_global_settings_wrapper', function() {
   // Do your stuff when 
}, 10, 0);
```

**Reference**

`do_action('fluentform/before_global_settings_wrapper');`

This action is located in `fluentform/app/Views/admin/settings/index.php`

</explain-block>

------------------------------------------------

<explain-block title="fluentform/after_global_settings_wrapper">

**Description**

After rendering the form settings page this hook is available.

**Usage:**
```php 
add_action('fluentform/after_global_settings_wrapper', function() {
   // Do your stuff when 
}, 10, 0);
```

**Reference**

`do_action('fluentform/after_global_settings_wrapper');`

This action is located in `fluentform/app/Views/admin/settings/index.php`

</explain-block>

------------------------------------------------

<explain-block title="fluentform/before_form_settings_app">

**Description**

This action fires before fluentform plugin rendered.

**Parameters**
- `$form_id` (int) Form ID

**Usage:**
```php 
add_action('fluentform/before_form_settings_app', function($form_id) {
   // Do your stuff when 
}, 10, 1);
```

**Reference**

`do_action('fluentform/before_form_settings_app', $form_id);`

This action is located in `fluentform/app/Views/admin/form/settings.php`

</explain-block>

------------------------------------------------

<explain-block title="fluentform/after_form_settings_app">

**Description**

This action fires after fluentform plugin is loaded.


**Parameters**
- `$form_id` (int) Form ID

**Usage:**
```php 
add_action('fluentform/after_form_settings_app', function($form_id) {
   // Do your stuff when 
}, 10, 1);
```

**Reference**

`do_action('fluentform/after_form_settings_app', $form_id);`

This action is located in `fluentform/app/Views/admin/form/settings.php`

</explain-block>

-----------------------------------------

<explain-block title="fluentform/before_global_settings_option_render">

**Description**

This action fires on each global settings component before rendering the page.

**Usage:**
```php 
add_action('fluentform/before_global_settings_option_render', function() {
   // Do your stuff when 
}, 10, 0);
```

**Reference**

`do_action('fluentform/before_global_settings_option_render');`

This action is located in `fluentform/app/Views/admin/settings/settings.php`

</explain-block>

-----------------------------------------

<explain-block title="fluentform/after_global_settings_option_render">

**Description**

This hook is available before rendering the global settings option page. Fore example Custom CSS/JS page.

**Usage:**
```php 
add_action('fluentform/after_global_settings_option_render', function() {
   // Do your stuff when 
}, 10, 0);
```

**Reference**

`do_action('fluentform/after_global_settings_option_render');`

This action is located in `fluentform/app/Views/admin/settings/settings.php`

</explain-block>

------------------------------------------

<explain-block title="fluentform/form_settings_container_{$current_route}">

**Description**

This hook runs before rendering the settings page container.

**Parameters**
- `$form_id` (int) Form ID

**Usage:**
```php 
add_action('fluentform/form_settings_container_{$current_route}', function($form_id) {
   // Do your stuff when add fluentform admin menu
}, 10, 1);
```

**Note:** `{$current_route}` is a dynamic settings route. Replace `{$current_route}` with Fluent Forms settings route.

**Reference**

`do_action('fluentform/form_settings_container_' . $current_sub_route, $form_id);`

This action is located in `fluentform/app/Views/admin/form/settings_wrapper.php`

</explain-block>

------------------------------------------

<explain-block title="fluentform/global_settings_component_{$current_component}">

**Description**

This action fires on each global settings component. For example reCaptcha

**Usage:**
```php 
add_action('fluentform/global_settings_component_{$current_component}', function() {
   // Do your stuff when add fluentform admin menu
}, 10, 0);
```

**Note:** `{$current_component}` is a dynamic component name. Replace `{$current_component}` with Fluent Forms component name.

**Reference**

`do_action('fluentform/global_settings_component_' . $currentComponent);`

This action is located in `fluentform/app/Views/admin/settings/index.php`

</explain-block>




