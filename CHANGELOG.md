# Changelog

## 2019-03-27

* Allow site editors to manage domain settings (except adding, removing and DNS management) and SSL certificates.
* Liquid: Add `position`, `created_at` and `updated_at` attributes in ElementDrop ([read more](https://www.voog.com/developers/markup/objects/element)).
* Render empty `sitemap.xml` response (with status 403) for suspended websites.

## 2019-03-15

* Ecomerce: Add payment gateway management interfaces (PayPal, MakeCommerce, offline invoice).
* General improvements in admin views.

## 2019-03-01

* Update domain price list.
* Improved site asset search when filename contains `.`.

## 2019-02-13

* Add timezone information to form ticket email.
* Add direct link from single ticket view to the related form listing.
* Add missing form file input field data to CSV export file.
* Liquid: Add accessibility related texts to translations ([read more](https://www.voog.com/developers/markup/basics/i18n#built-in-translations)).
* Ecommerce API: Fixed missing product object in BuyButton API.
* Ecommerce: Use Voog e-mail in the FROM field of ecommerce customer e-mails.
* Improved referrer code handling on signup.

## 2019-01-30

* Fixed Voog internal site indexing for nested structures (e.g. tables).
* Ecommerce: Added custom event for shopping cart shipping methods (`voog:shoppingcart:showshippingmethods`) ([read more](https://www.voog.com/developers/scripting/ecommerce/shopping-cart)).
* Ecommerce: Allow editor to re-enable the ecommerce module if allowed by the subscription plan (Premium).

## 2019-01-16

* Ecommerce: Orders export (XLS, CSV) now outputs all orders (instead of 50 latest)
* Other minor tweaks and fixes

## 2019-01-03

* Support IPv6 in form ticket data
* Ecommerce: Improve BuyButton rendering in edit mode
* Fixed checkbox label padding for settings editor

## 2018-12-19

* Ecommerce: Fixed large buy button (with price) rendering in mobile views.
* Add HTTP `X-Robots-Tag` support for pages and articles. Allow to set `robots_header` value with Page and Article API.
* Liquid: Support `tag` filter attribute in article `load` tag like in Articles API. [Read more](https://www.voog.com/developers/markup/tags/load#load_tag).
* Liquid: Add `published?` method to Liquid `Article` drop. [Read more](https://www.voog.com/developers/markup/objects/article#article_published).
* Updates for Voog support chat.

## 2018-12-11

* New Voog support chat.

## 2018-12-06

* Improve elements filter related query performance.
* Ecommerce: Minor ShoppingCart code improvements.
* Sanitize `undefinded` to `null` in page/article custom data values (`Edicy.articles.currentArticle.setData(key, value)` and `Edicy.CustomData.set`).

## 2018-11-21

* Ecommerce: Fixed issue where `order.items_original_amount` wasn't sometimes rounded correctly.
* Ecommerce: Fixed issue where order cancelled email was sent to shop owner in case of MakeCommerce transaction initialization and pending events..
* EdicyTools: Replace throw statement with console.error.
* Fixes save button feedback in elements admin view.

## 2018-11-13
* Cache `/favicon.ico` 404 response for 1 hour.
* Ecommerce: Improved buy button rendering.

## 2018-11-08

* Fixed OG image url scheme for API https request responses (Article, Page, MediaSets)
* Improved caching in elements API listing response
* Fixed issue where `og:url` domain in public views doesn't always match with request domain name
* Fixed site cache swiping on elements reordering and page duplication
* Give immediate feedback about loading the page settings modal
* Fix double languages in structure view
* Fixed language publishing toggle
* Image drop area plugin: Fixed plugin to work correctly with `positionable` attribute (https://github.com/Voog/voog/issues/14)
* Settings Editor plugin : Add tooltips support ([read more](https://www.voog.com/developers/scripting/javascripts/settings-editor))
* Settings Editor plugin: Add toggle as item type ([read more](https://www.voog.com/developers/scripting/javascripts/settings-editor))
* Other minor tweaks and fixes

## 2018-10-24

* Add `region` field (e.g. `GB`) to language object (accessible via liquid)
* Liquid: Add `region` and `locale` to `Language` object ([read more](https://www.voog.com/developers/markup/objects/language))
* Liquid: Add `language_region` and `language_locale` to `Page` object ([read more](https://www.voog.com/developers/markup/objects/page))
* Ecommerce: Display descriptive low stock error messages in shopping cart
* Ecommerce: Add information about shipping address to order emails
* Ecommerce: Improved number input format in store admin views
* Ecommerce: Fixed Nordea bank logo for Finnish customers in cart
* Show full asset name in file panel
* Close "Add" and "Files" panel when user clicks on menubar
* Add toggle type indicators to design editor
* Fixed issue where user invite emails was always sent out in English
* Do not redirect pages with `page.permanent_redirect_url` value in edit and preview mode.
* Add GDPR DPA link to user profile view
* Improved edicy-tools widgets stability

## 2018-10-17

* Ecommerce: Allow store management (including API access) always when ecommerce feature is enabled in plan
* Fixed datepicker wrong month value

## 2018-10-12

* Ecommerce: Add default filtering for archived orders
* Improved application stability
* Other minor tweaks and fixes

## 2018-09-28

* Improved assets related thumbnails preloading performance
* Add `minWidth` and `minHeight` options to gallery lightbox

## 2018-09-12

* Add delete button to text area and image toolbars
* Add unique `X-Entity-Ref-ID` SMTP header to form ticket emails to prevent threading in Gmail
* Use human-readable Unicode domain name in admin view title bars
* Improve browser-side favicon caching
* Ecommerce: Fixed discount calculation for fixed values (cart and cart with shipping discounts)
* Ecommerce: Update customer payment confirmation email copy

## 2018-08-29
 
* Display data usage as percent in assets view
* Force global match in file picker filter
* Allow trial plan user to select a plan when buying domains
* Improved elements reordering performance
* Ecommerce: Add alignment dropdown to the buy button toolbar

## 2018-08-15

* Liquid: `load` tag improvements ([see more](https://www.voog.com/developers/markup/tags/load)):
  * Support variables in attributes
  * Support [query filtering](https://www.voog.com/developers/api/basics/filters) syntax like in [Voog API](https://www.voog.com/developers/api)
  * Add alias types `media_set` and `media_sets` for legacy types `mediaset` and `mediasets`.
  * Add support to new load types: `article` (load [Article object](https://www.voog.com/developers/markup/objects/article)) and `articles` (loads array of Article objects).
  * Add attribute `limit` to limit objects loaded by `media_sets` and `articles` type.
  * Examples:

Legacy syntax (media sets only):
  
```
{% load mediaset to "my_gallery" title="Foobar" %}
```

New syntax:

 ``` 
{% load media_set to "my_set" q.media_set.title.$eq="Foobar" %}
{% load article to "my_article" q.article.title.$eq="Foobar" %}
{% load articles to "my_articles" q.page.id=page.id limit=10 %}
 ```
* Ecommerce: Add filter to products admin view.
  

## 2018-08-08

* Improve elements and element relation-related performance
* Fixed issue with newly provisioned SSL certificate always showing "waiting" status
* Updated copy of the tell-a-friend email

## 2018-08-01

* Liquid: Support "invisible" flag in content area. Area with this flag is invisible until it shows drop place holder when user starts to drag some content area. Example:
```
{% content name=""invisible-content-area" invisible=true %}
```
* Fix catalogue element drag placeholder position in admin view
* Improve domain expiration notifications in admin domains view
* Fixed S3 "cache-control" value for thumbs and static.voog.com lib files
* Set static.voog.com lib assets cache "max-age" value to 1 year for versioned files and 1 day for "latest".
* Use versioned url for injected "picturefill.js" file url

## 2018-07-19
- Ecommerce: Product variant values are now properly translatable
- Ecommerce: Add a link to the store settings view to the settings menu
- Liquid: Add the `invisible` parameter to the `content` tag to create content areas without visible placeholders:
  - `{% content invisible="true" %}`
- API: Add ?include_body=true parameter to the Layouts API index request
- Warn the user if they're trying to delete or hide the last visible language on their site
- UX improvements in the domain security view

## 2018-07-06

- Update Image Drop Area widget to support relative positioning
- Update text area parser rules
- Use modal to add new articles on /admin/content/articles?blog=ID pages
- UX improvements in the /admin/stats/sources view
- Minor UX improvements to the form editor
- Correct calculations in /admin/stats/sources view
- Liquid: Update `addbutton` tag to work inside `blogcontext` blocks
- Ecommerce: Cosmetic improvements to the pagination components
- Ecommerce: Update payment methods view to link to relevant articles
- Ecommerce: Fix adding discounts to specific products
- Ecommerce API: Add `sku` to CartItem API response

## 2018-06-20

- Include articles and elements when duplicating the front page
- Referral view bug fixes
- Various cosmetic and UX tweaks to admin views and editmode widgets
- Leave site structure uncollapsed when duplicating a subpage
- Update robots.txt parsing rules on site indexing
- Fix embedded content block to make the inserted content editable
- Updated embedded content parsing rules when calculating iframe width
- Updated embedded content parsing rules to accept comments and textnodes as we
- Hide page settings modal when deleting the page from the Structure view
- Fix form button to show its custom submit text
- Fix wall-type gallery rendering
- Add visual feedback to the save button to reflect the unsaved and saving states
- Blacklist the Unicode control characters (`U+2028` and `U+2029`) in the text editor
- Use modal to add articles from blogs admin view
- Ecommerce: Add pagination to Order list and Product list views
- Ecommerce: Add pagination to Order and Product API
- Ecommerce: Show translated values in the product view in the current language context
- Liquid: Update the addbutton tag to accept variable parameters:

```
{% addbutton page_id=element.page_id element_type=element.model_name %}
```

```
{% blogcontext "my_blog" %}
  {% addbutton page_id=blog.page.id %}
{% endblogcontext %}
```
- API: Fixed Assets API to take current protocol into account when returning the upload URL

## 2018-06-12

- Fixed bug with changing the current design template right after signing up

## 2018-06-07

- Allow adding custom classes to forms
- Cosmetic tweaks to various modals
- Ecommerce: Fixed "translate" button in ecommerce views to properly open the translation modal
- API: Remember the last customized design template name and customization timestamp, accessible via /admin/api/site
- API: List `offline` payment gateway in Ecommerce Gateways API
- API: Allow to disable `offline` payment gateway
- API: Support sorting by product translated values when a language context is given

## 2018-05-25

- Update Tell A Friend referral URLs
- GDPR-related additions — terms acceptance/marketing consent modals etc.

## 2018-05-02

- Remove deprecation warning from components using Google Maps
- Fixed form ticket checkbox rendering

## 2018-04-25

- Fix social media widget
- Ecommerce: support using the `order.note` field both in the shopping cart and in the Order view
- Ecommerce: various UX improvements
- Ecommerce: Visual twaks to required fields in the shopping cart

## 2018-04-11

CMS:

- Fixed page settings modal to properly handle unsuccessful updates
- Fixed account expiration email rendering

## 2018-03-23

CMS:

- Updated refer view copy
- Ecommerce: Fixed shipping cost calculation in the shopping cart
- Ecommerce: Fixed a rounding bug that caused failing checkouts in some cases
- Ecommerce: Tweaked variant selection in the Product view

## 2018-03-21

- Prevent multiple 301 redirects when the domain is set to prefer the www form
- Fixed bug with the "all time" filter in the statistics view
- Fixed custom 404 page rendering with no visible languages

## 2018-03-01

- Liquid: Added `sign_out` key to [translations](https://www.voog.com/developers/markup/basics/i18n)

## 2018-02-02

- Ecommerce: Fixed store creation for Standard and Plus plan editors

## 2018-01-29

- Prevent domain redirect loops
- Ecommerce: changed offline payment receiver to company name instead of store name
- Ecommerce: fixed Product caching issues

## 2017-12-22

- Ecommerce: Fix some discount-related texts in emails and on invoices
- Ecommerce: Improve multi-page invoices
- Ecommerce: Allow unicode characters in discount codes

## 2017-12-19

* Ecommerce: Implement discounts. [Read more](https://www.voog.com/developers/api/ecommerce/discounts)
* Fixed bug with changing months in catalog tool datepicker ([#1](https://github.com/Voog/voog/issues/1))

## 2017-11-23

* Liquid: Fixed issue where `{{ elements | json }}` fails.
* Liquid: json filter now returns same object files for array of liquid objects (like `{{ elements | json }}`) and single object `{{ elements | json }}`. Fixes issue where in some case internal object attributes was present in json output.
* Liquid: Fixed issue where `{{ site.latest_articles | json }}` raises error.

## 2017-11-22

* Liquid: Support `readonly=true` attribute in `content` and `contentblock` tags. [Read more](https://www.voog.com/developers/markup/tags/content#readonly). Example:

```
<div class="banner-area">{% content name="banner-area" readonly=editmode %}</div>
{% if editmode %}<div class="banner-area-edit-mode">{% content name="banner-area" %}</div>{% endif %}
```

* Liquid: Support objects in `bind` attribute for `content` and content block tags. Suuported objects: `Article`, `Element`, `Language` and `Page`. [Read more](https://www.voog.com/developers/markup/tags/content#bind). Example:
```
{% elementscontext q.element.values.category.$in="Books" s="element.values.date.$asc" %}
  {% for el in elements %}
    <a href="{{ el.url }}">{{ el.title }}</a>
    <div class="gallery">{% content name="content-gallery" bind=el %}</div>
  {% endfor %}
{% endelementscontext %}
```

```
{% for lang in site.languages %}
  {% if lang.code == "en" %}
    {% content name="banner" bind=lang %}
  {% endif %}
{% endfor %}
```

* Liquid: Fixed issue where new fields couldn't be added to element definitions that had only element relations defined
* Liquid: Fixed `reorder` and `group` tags to also work with `article.title`.
* SettingsEditor: Add new types: `number`, `range`, `text` and `textarea` [Read more](https://www.voog.com/developers/scripting/javascripts/settings-editor).
* Ecommerce: Fix invoice value date not displaying the correct value in the store settings view

## 2017-10-26

* SEO: Add alternate language (`rel="alternate"`) links to sitemap.xml. [Read more](https://support.google.com/webmasters/answer/2620865).
* SEO: Allow sites photos/files to be indexed by search engines by default on Voog media host (media.voog.com)
* Liquid: New Liquid tag `sd_breadcrumbs` for generating JSON-LD breadcrumbs. [Read more](https://developers.google.com/search/docs/data-types/breadcrumbs). Usage:

```
{% sd_breadcrumbs %}
=> <script type="application/ld+json">{"@context":"http://schema.org","@type":"BreadcrumbList","itemListElement":[{"@type":"ListItem","position":1,"item":{"@id":"http://test.voog.com/en","name":"Home"}},{"@type":"ListItem","position":2,"item":{"@id":"http://test.voog.com/contact","name":"Contact"}}]}</script>
```
* API: Add `updater` attributes to [Layout](https://www.voog.com/developers/api/resources/layouts) and [LayoutAssets](https://www.voog.com/developers/api/resources/layout_assets) API responses
* API: Password-protected resources are now accessible for logged-in users
* Render custom error layouts only if site actively uses a custom design
* Allow IP addresses for link-type menu item destinations
* Various performance improvements
* Various visual improvements
* Other minor tweaks and fixes

## 2017-10-11

* Liquid: Add `json_parse` filter ([read more](https://www.voog.com/developers/markup/basics/filters#json_parse):
```
{% assign json_result = '{"foo":{"bar":[1,2,3]}}' | json_parse %}
  
  Result: {{ json_result.foo.bar.last }}<br>
  
  {% for el in json_result.foo.bar %}
    {{ el }}<br>
  {% endfor %}
```
* Liquid: Add support for array filters like `push`, `pop`, `shift` and `unshift`. [Read more](https://www.voog.com/developers/markup/basics/filters#array-filters).
* Liquid: Upgraded Liquid to latest stable version (v4.0.0)
  * Support Range Type (`{{ assign nums = (x..y) }}`)([Shopify/liquid#761](https://github.com/Shopify/liquid#761))
  * Add whitespace control characters (`{{-` and `{%-`) ([Shopify/liquid#773](https://github.com/Shopify/liquid#773))
* Other minor tweaks and fixes

## 2017-09-27

* Ecommerce: XLS and CSV export for products
* Ecommerce: Improved rendering for multi-pate PDF invoices
* Ecommerce: improved admin mobile views
* API: Add `parent_id` and `parent_type` as aliases for content partial's `page_id` and `page_type`
* Updated BuyButton API docs
* Allow site editors to delete other editors
* Add IDNA support for free domain names (e.g. "õäöü.voog.com")
* Other minor tweaks and fixes

## 2017-09-15

* Ecommerce: Prevent showing "out of stock" badge when stock is actually unlimited
* Elements: Allow removing belongs_to references for related elements
* Fixed sorting of SSL certificates
* Other minor tweaks and fixes

## 2017-09-13

* Ecommerce: Fixed disabling product variants
* Ecommerce: Improved plan-based product limits and relevant error messages
* Liquid: Unify `Element`  object attributes and `to_json` output
  * Add `path` and `path_with_page` to `Element`object
  * Add `url` and `model_name` to `Element` object `to_json` output
* Don't trim whitespace from PlainTextEditor contents on initialization
* API: Improved API cache cleaning in inventory management context
* Fixed JS error in edit mode caused by Chrome v61 update
* Other minor tweaks and fixes

## 2017-09-05

* Ecommerce: Implement basic inventory management
* Improved SSL certificates view and custom certificate upload form
* Allow removing Voog footer from store invoices (on request)
* Various visual tweaks
* Other minor tweaks and fixes

## 2017-08-17

* Ecommerce: Improved ordering in transactions report view
* Ecommerce: Translation modal improvements
* Ecommerce: Fix shipping method availability dropdown
* Added domain redirect info to domain list
* Visual tweaks in domain views
* Live chat improvements
* Other minor tweaks and fixes

## 2017-08-14

* Improved behaviour for the 'force SSL' dropdown in domain settings view
* Disable redirecting domain while the Let's Encrypt validation is still pending
* Other minor tweaks and fixes

## 2017-08-09

* Thoroughly updated all domain views and added SSL security view
* Ecommerce: visual tweaks
* Various visual fixes
* Other minor tweaks and fixes

## 2017-07-21

* Ecommerce: Implement importing product variant types from other products
* Ecommerce: Improved transaction report views
* Support Let's Encrypt verification requests
* Display "pointer" cursor on gallery items in public mode
* Enable translating buy buttons and store settings in editmode modals
* Other minor tweaks and fixes

## 2017-07-17

* Ecommerce: Enable ecommerce in all plans (with transaction fee in some plans)
* Ecommerce: Fixed adding new shipping methods
* Added information about SSL certificates to plans view

## 2017-07-10

* Added live chat with customer support
* API: Improved Elements caching
* API: Allow posting arrays as element values
* Ecommerce: Added `paid_at` field to Orders

## 2017-06-22

* Improved site language autodetection fallbacks
* API: Fixed issue where `image_id` was rejected from Page create request
* removed pages under hidden languages from sitemap.xml
* Ecommerce: Added XLS and CSV exports for Orders
* Ecommerce: Add (optional) terms and services agreement checkbox to the shopping cart.
* Ecommerce: product list view improvements

## 2017-06-07

* Ecommerce: Add "translate" button and tooltips to product view
* Ecommerce: Translate product statuses in products list
* Liquid: Fixed scoping issue with `reorder` and `assign`
* Other minor tweaks and fixes

## 2017-05-24

* Ecommerce: Visual improvements for the product view
* Ecommerce: Add support for new payment methods: `liisi_ee`, `saastopankki`, `spankki` and `tapiola`.
* Ecommerce: Minor bugfixes for store address fields
* Fixed uploading assets on IDNA domains (IE)
* Fixed text editor toolbar to the top of the viewport
* Fixed signup link in sites management menu
* Other minor tweaks and fixes

## 2017-05-10
* Ecommerce: Behaviour tweaks for variant editor in product details view
* Ecommerce: Visual tweaks in variant list component in product details view
* Ecommerce: Minor bugfixes and tweaks
* Ecommerce: Updated API documentation [/developers/api/ecommerce/carts](https://www.voog.com/developers/api/ecommerce/carts)
* Ecommerce: Visual fixes to translation modal in store settings view
* Liquid: Limit actual size of extremely long `articles` arrays (affects only the default `articles` variable)
* Update domain pricing and add some new domains (ch, cn, es, io, nu, se, vc, xyz)
* Fixed text editor 'justify' behaviour
* Fixed problematic search behaviour for uploaded images with incorrect mime types
* Added new events to shopping cart: [/developers/scripting/ecommerce/shopping-cart](https://www.voog.com/developers/scripting/ecommerce/shopping-cart)
* Changed all form labels to allow unescaped HTML as contents
* Minor tweaks to intro tour
* Popover positioning tweaks

## 2017-04-26
* API: Allow adding Languages with custom codes ('eu', 'gb' etc.)
* API: Allow creating elements by `element_definition_title` instead of id
* Ecommerce: Fix terms and services link in shopping cart
* Ecommerce: Properly remove deleted products from products list (Voog/voog#5)
* Ecommerce: Orders view style improvements
* Ecommerce: Support both `language` and `language_code` parameters for API requests
* Ecommerce: Set default country code when creating a new store
* Ecommerce: Hide shipping method details when there are no description and options defined
* Ecommerce: Add status field to product list view
* Ecommerce: Add `tax_rate` field to all Product API responses
* Ecommerce: Add new public methods to global JS objects:
  * `Voog.buyButtonsManager`: `refreshSelectedVariants` ,`setState` ,`setPrice` ,`setPickedVariants`
  * `Voog.ShoppingCart`: `addProductById`
* Visual improvements to draggable elements
* Social media icon improvements:
  * option to open links in a new tab
  * better support for small screens
  * fix FB share button
* Other minor tweaks and fixes

## 2017-04-13
* Ecommerce: Visual tweaks and fixes to product and settings views
* Ecommerce: Buy button tweaks in editmode
* Ecommerce: Limit total count of enabled product variants to 200
* Ecommerce: Visual tweaks to buy button and its settings popover
* Ecommerce: Check product availability before submitting shopping cart
* Other minor tweaks and fixes

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
