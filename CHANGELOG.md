# Changelog

## 2017-03-30
* Support variables as parameter values in custom Liquid tags (`elementscontext`, `blogcontext`, `content`, `contentblock`, `xcontent`)
* Changed element filtering `$match`, `$starts` and `$end` filters to be case insensitive
* Fixed bug with multiple social media content blocks
* Ecommerce: Fixed variant info shown in order details view for products without variants
* Ecommerce: Fixed text inputs in translation modals
* Ecommerce: Fix form input errors and required field indicators
* Other minor tweaks and fixes

## 2017-03-23
* Updated new article button behaviour in the toolbar's "Content" menu
* Fixed toolbar for IE and older Safari versions
* Ecommerce: Added support for product variants
* Ecommerce: Improve API caching for ecommerce endpoints
* Ecommerce: Various buy button style and behaviour tweaks
* Ecommerce: Various tweaks and fixes to product variant views
* Other minor tweaks and fixes

## 2017-03-01
* Changed `{% addbutton %}` to open a modal form instead of navigating to an empty view
* Various social media content area tweaks:
added alignment tool
  * improved popover positioning
  * added support for LinkedIn, SoundCloud and Spotify
* Ecommerce: Tweaked various shopping cart inputs and styles
* Ecommerce: Removed language button from buy button modal
* Other minor tweaks and fixes

## 2017-02-15
* Made image drop areas open filepicker menu when clicked
* Re-added "justify" to text alignment tools due to popular demand
* Fixed DNS record case sensitivity bugs
* Ecommerce: Fixed some tax calculations
* Ecommerce: Improved invoice rendering
* Ecommerce: Added tabbed navigation to admin views
* Ecommerce: various style tweaks
* Ecommerce: Added maximum width to invoice logo images
* Ecommerce: Improved buy button price formatting
* Other minor tweaks and fixes

## 2017-02-01
* Removed user invite limitations from expired Trial sites
* Fixed z-index issues with gallery image link tool
* Included hidden pages in `sitemap.xml`
* Mobile: Improved headers in statistics views
* Ecommerce: Made shopping cart button rendering trigger the `voog:shoppingcart:button:created` event
* Ecommerce: Made products translatable in editmode and admin views
* Ecommerce: Added custom VAT support to shipping methods
* Ecommerce: Added customer phone number to payment notifications
* Other minor tweaks and fixes

## 2017-01-19
- Fix reordering links in structure view
- Fix uploading to selected media set
- Fix image to_json method in `PageDrop` and `ArticleDrop`
- Add affiliate code input to site settings
- Ecommerce: Add multilingual support for online store settings
- Ecommerce: Allow to set custom logo for online store
- Ecommerce: Product locations in online store’s product details view
- Ecommerce: Add full error messages to online store settings
- Ecommerce: Fix online store’s archived order style and dropdown
- Ecommerce: Add `note` attribute to `CartItem` and `OrderItem` models

## 2016-12-22
* Ecommerce: Add product management views
* Ecommerce: Show "Invoice paid up" label on paid invoices
* Ecommerce: Add user payment method to order details view
* Ecommerce: Add tooltips to store settings view
* CMS user experience improvements

## 2016-12-20
* Ecommerce: Add order code formating support (prefix, suffix, padding, starting from)
* Ecommerce: Shopping cart improvements
* Ecommerce: Fix order filtering
* Liquid: Add `layout_title` to `menuitem` and `page` drops
* Liquid: Improved `menubtn` function. It supports now any menuitem arrays (not only hidden menuitems)
* Liquid: Added `{{ site.untranslated_children }}` and `{{ site.untranslated_children_with_data }}` to `site` drop
* Fixed issue where link page can't be destroyed in some cases
* Added designs categories to Voog signup view ("Website", "Online store", "Blog")

## 2016-12-16
* Ecommerce: Add Maksekeskus (MakeCommerce) payment gateway support
* Ecommerce: Remove products from buy buttons when duplicating the page with buy buttons
* Ecommerce: Send email notification to shop admin for all pending and cancelled notifications
* Ecommerce: Always send paid invoice notifications to customers when the store admin has manually marked the order as 'paid'
* Ecommerce: Invoice tweaks
* Fix Firefox opening social share page in the same window

## 2016-12-12
* Ecommerce: Add PayPal Standard Payment payment gateway support
* Ecommerce: Add shipping methods support
* Ecommerce: Hide unconfigured buy buttons from public view
* Ecommerce: Add different button text styles to buy button settings

## 2016-12-09
* Fixed issue where `elementscontext` parameters rejected blank values, e.g `edicy_page_path=''`
* Make the whole order row navigate to detail view when clicked
* Ecommerce: Improved shopping cart and shop admin views
* Ecommerce: Allow to select/change/delete existing products in button settings

## 2016-11-23
* Fixed issue where `elementscontext` block was ignoring `s` sorting attribute
* Fixed bug with updating elements' number fields in admin views
* Fix popover menu item width and positioning on small (<375px) screens
* Add `getNativeElement` function for `imgDropArea` plugin. Adds support for binding the image drop area with the following syntaxes: `$('selector')`, `$('selector').get(0)`, `document.querySelector('selector')`, `document.querySelectorAll('selector')`
* Allow adding assets directly to mediaset in Assets API confirmation requests, using `media_set_id` parameter
* Search widget now calculates the max height of the modal dynamically
* CMS user experience improvements
* Ecommerce: Improved shopping cart and shop setup flow
* Ecommerce: Add store payment status and order creation notification emails

## 2016-11-09
* Add more social media channels to social media content button (LinkedIn, Medium, Tumblr, Vimeo, VKontakte, Youtube)
* Improved content area border rendering in edit mode
* Fixed tag editor autocomplete for sites with more than 250 tags
* CMS user experience improvements
* Ecommerce bug fixes and user experience improvements

## 2016-10-26
* Liquid: Add alternative (utf8) string filters `upcase_utf8`, `downcase_utf8`, `capitalize_utf8`
* CMS user interface improvements
* Ecommerce: Improvements and fixes
* Improved wall-type gallery rendering when padding is defined
* Domain expiration notification improvements

## 2016-10-17
* Initial release of the Voog Ecommerce engine
