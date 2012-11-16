Required Fields
===============

Adds an extensible API and some basic settings to WordPress to make standard fields on the post edit screen required before a post can be published.

Head to the **Writing** settings page and scroll to the bottom. There you will find boxes to check to make certain fields required when a user adds or edits a post or page.

The default options are to make the title, content, custom excerpt and category mandatory.

## API

There is an API to add your own required fields too:

```php
/**
 * Registers a field as required for a post to be published.
 * The default callback checks if the value of the post data or
 * post meta field corresponding to the $name is empty or not.
 *
 * @param string $label               Nice name for the required field
 * @param string $name                The post data array key or custom field key eg: 'post_title', 'my_meta_key'
 * @param string $message             The error message to display if validation fails
 * @param function $validation_cb     A callback that returns true if the field value is ok
 * @param string|array $post_type     The post type or post types to run the validation on
 *
 * @return void
 */

register_required_field( $label, $name, $message, $validation_cb, $post_types );
```

Any questions or problem give me a shout on Twitter [@sanchothefat](http://twitter.com/sanchothefat)
