# Course Product Manager

A WordPress plugin to manage relationships between MasterStudy LMS courses and WooCommerce products.

## Description

Course Product Manager simplifies the process of linking MasterStudy LMS courses with WooCommerce products, allowing you to sell courses and webinars through your WooCommerce store.

## Features

- Link STM courses with WooCommerce products
- Manage two product types per course:
  - Course Product (for direct course purchase)
  - Webinar Product (for webinar access)
- Quick edit relationships without page reload
- Create new products directly from the plugin
- Search and filter courses
- Bulk relationship management
- Automatic ACF field updates for purchase links

## Requirements

- WordPress 5.0 or higher
- WooCommerce 3.0 or higher
- MasterStudy LMS Plugin
- PHP 7.2 or higher

## Installation

1. Download the plugin files
2. Upload the `course-product-manager` folder to `/wp-content/plugins/`
3. Activate the plugin through the 'Plugins' menu in WordPress
4. Navigate to 'Course Products' in your WordPress admin menu

## Usage

### Adding a New Relationship

1. Go to **Course Products > Add New**
2. Select a course from the dropdown
3. Choose the product type (Course, Webinar, or Both)
4. Either select an existing product or create a new one
5. Click "Create Relationship"

### Managing Existing Relationships

1. Go to **Course Products > All Relationships**
2. Use the search box to find specific courses
3. Click "Quick Edit" to modify relationships
4. Use "Add Product" or "Remove" links for quick changes

### Product Creation

When creating a new product through the plugin:
- Products are automatically set as "simple" products
- Stock status is set to "in stock"
- Products are linked bidirectionally with courses

## Developer Information

### Hooks and Filters

The plugin uses standard WordPress hooks:
- `init` - Plugin initialization
- `admin_menu` - Admin menu registration
- `admin_enqueue_scripts` - Script and style loading
- `wp_ajax_*` - AJAX handlers

### Database

The plugin stores relationships using WordPress post meta:
- `related_course_product_id` - Course product relationship
- `related_webinar_product_id` - Webinar product relationship
- `related_stm_course_id` - Reverse relationship on products

### ACF Integration

If ACF is installed, the plugin updates:
- `field_6821879221940` - Course product purchase link
- `field_6821879e21941` - Webinar product purchase link

## Support

For support and bug reports, please create an issue on GitHub.

## License

GPL-2.0+

## Credits

Developed by Lucuma Agency