# Changelog

## 2023-11-29

- Designs: Introduced new barebones theme for developers – [Wellington](https://github.com/Voog/design-wellington).

## 2023-11-27

- Ecommerce: Support multiple product assets in the admin interface, [Products API](https://www.voog.com/developers/api/ecommerce/products) and [Liquid](https://www.voog.com/developers/markup/ecommerce-objects/product) and in the canonical product page fallback
design.
- Liquid: Add the [`assets`](https://www.voog.com/developers/markup/ecommerce-objects/product#product_assets) and [`photos`](https://www.voog.com/developers/markup/ecommerce-objects/product#product_photos) methods to the [Product object](https://www.voog.com/developers/markup/ecommerce-objects/product).
- Liquid: Product [`image`](https://www.voog.com/developers/markup/ecommerce-objects/product#product_image) now returns an [Asset](https://www.voog.com/developers/markup/objects/asset) instead of an [Image](https://www.voog.com/developers/markup/objects/image).
- Liquid: Add the [`gallery`](https://www.voog.com/developers/markup/tags/gallery) tag.
- Liquid: `page.path` now returns the full path of the request in context of the custom 404 layout.

## 2023-11-09

- Fix domain purchase failure when the TLD did not include a 1Y period.

## 2023-11-07

- Ecommerce: Implement filtering orders by discount codes.
- Ecommerce: Implement exporting discounts as XLSX (optionally with associated orders).
- Ecommerce: Combine bulk exported shipping labels into a single PDF.
- Ecommerce: Include canonical product page content areas in the [Contents API](https://www.voog.com/developers/api/resources/contents).
- Liquid: Fix `title` tag rendering in custom 404 layouts.

## 2023-11-13

- Ecommerce: Update MakeCommerce payment method icons.

## 2023-10-22

- Liquid: Add `content_type` to the [Asset object](https://www.voog.com/developers/markup/objects/asset#asset_content_type).

## 2023-10-11

- Ecommerce: Redesign discount management admin views.
- Ecommerce: Display product SKU in emails.
- API: Add pagination support and new fields (`orders_count`, `redeemable`) to the [Discounts API](https://www.voog.com/developers/api/ecommerce/discounts).
- Liquid: Fix a bug converting `site.menuitems` to JSON.

## 2023-10-06

- Liquid: Add the `lookup_page_id` and `lookup_path_prefix` parameters to the [`editable`](https://www.voog.com/developers/markup/tags/editable) tag for use with element relation fields.
- Liquid: Add the optional `values` parameter to the [`addbutton`](https://www.voog.com/developers/markup/tags/addbutton) tag for pre-filling fields at element creation.

## 2023-09-24

- Ecommerce: Introduce sale price management, including support for sale price in buy buttons, on-site shopping cart, checkout, product list content areas, and canonical product pages.
- API: Add fields related to sale price management (`sale_price`, `effective_price`, `effective_price_min`, `effective_price_max`, `on_sale`) to the [Products API](https://www.voog.com/developers/api/ecommerce/products).
- Liquid: Add new fields to the [Discount object](https://www.voog.com/developers/markup/ecommerce-objects/discount).
- Liquid: Add new fields to the [Product object](https://www.voog.com/developers/markup/ecommerce-objects/product).
- Liquid: Add new fields to the [Product List object](https://www.voog.com/developers/markup/objects/product-widget).
- Liquid: Add the `discount` field to the [Order Item object](https://www.voog.com/developers/markup/ecommerce-objects/order-item).

## 2023-09-20

- Ecommerce: Improve cart field management for multilingual sites.
- Ecommerce: Implement product duplication.
- API: Add the [duplicate](https://www.voog.com/developers/api/ecommerce/products#duplicate_product) action to Products API.
- Fix the schema portion in site snapshot and orders export URLs.

## 2023-09-13

- Forms: Fix styling not being applied to new form fields until the page was reloaded.
- Ecommerce: Fix product title not displayed in the correct language in the on-site shopping cart.

## 2023-09-06

- Ecommerce: Redesign the email previews admin view.

## 2023-09-05

- Publish the redesigned [Voog Developers](https://www.voog.com/developers) documentation section.

## 2023-08-14

- Ecommerce: Enhance resolving category slug conflicts and transliterate non-Latin characters for slugs.

## 2023-08-03

- Ecommerce: Enhance store availability management in the store settings admin view.
- Ecommerce: Make various fixes to the checkout flow.
- Signup: Fix language selection.

## 2023-06-30

- Ecommerce: Redesign the store settings admin interface.

## 2023-06-27

- Allow users to remove their account from the site.

## 2023-06-14

- Ecommerce: Fix legacy shopping cart (v1) failure if selected shipping method's description is `null`.
- Liquid: Add the [`sd_product`](https://www.voog.com/developers/markup/tags/sd-product) tag.

## 2023-06-06

- Ecommerce: Introduce a new top-level store settings admin view.
- Ecommerce: Fix an bug in Makecommerce payment flow.

## 2023-06-02

- API: Introduce a new [Carts API index endpoint](https://www.voog.com/developers/api/ecommerce/carts#list_carts).
- Ecommerce: Trigger site indexing on various changes to the store.
- Enhance the page and product image picker with a collections filter and direct upload functionality.

## 2023-05-26

- API: Enable reordering payment types (`preferred_payment_types`) in checkout via the [Store settings API](https://www.voog.com/developers/api/ecommerce/store_settings#update_settings).

## 2023-05-18

- Ecommerce: Add physical properties (width, height, length, weight) to the [Products API](https://www.voog.com/developers/api/ecommerce/products), [Liquid](https://www.voog.com/developers/markup/ecommerce-objects/product), product details admin view and the products bulk editor.
- Ecommerce: Add DPD delivery integration.

## 2023-05-09

- Fix an issue where the Save button did not commit changes from the [background picker](https://www.voog.com/developers/scripting/javascripts/bgpicker).
- Relocate the "Add New Site" button to the top of the Dashboard.

## 2023-05-05

- Ecommerce: Fix the payment processing service to not expect uppercase currency codes.

## 2023-05-03

- Include canonical product pages in on-site search results.
- Various improvements to on-site search indexing.
- API: Introduce a new `product` type for the [Search API](https://www.voog.com/developers/api/resources/search).

## 2023-04-28

- Ecommerce: Implement editing order details.
- Ecommerce: Implement order package label regeneration.
- Ecommerce: Add MakeCommerce payment methods (`siauliu`, `revolut`, `indivy-go`, `moki`, `moki3`, `bigbank`).
- Ecommerce: Update Montonio payment method icons.
- Ecommerce: Enhance shipping method selection performance in checkout.

## 2023-04-25

- Liquid: Add support for loading product list content areas via the [load](https://www.voog.com/developers/markup/tags/load) tag.
- Improve default language selection UX in the admin interface.
- Fix an HTML escaping issue in the form ticket e-mail.

## 2023-04-19

- Add canonical product pages to website export snapshot.

## 2023-04-10

- Ecommerce: Support numeric custom fields in checkout.
- Ecommerce: Fix a regression resulting in incorrect product inventory when updating order status.

## 2023-04-06

- Fix scrolling in Checkout, Signup, and Login views when using older iOS versions.
- Present sitemap.xml as a [sitemap index file](https://developers.google.com/search/docs/crawling-indexing/sitemaps/large-sitemaps) referring to sitemap files for each type (pages, articles, products).
- Ecommerce: Add search engine indexing control for canonical product pages.
- Ecommerce: Include canonical product pages in the sitemap and allow controlling inclusion in the SEO admin view.
- Ecommerce: Improve checkout's payment tab's UX.
- Ecommerce: Allow limiting available countries in checkout.
- Ecommerce: Hide checkout's shipping tab if no enabled shipping methods available.
- Ecommerce: Improve mobile navigation in store admin views.
- Ecommerce: Improve paid label visibility in Order views.
- Ecommerce: Improve product list content area's catalogue view's UX.
- Ecommerce: Improve product detalis admin view preview button behavior.
- Ecommerce: Fix Stripe payment gateway integration for new Stripe accounts.

## 2023-03-24

- Ecommerce: Fix issues with the EveryPay payment provider if signed up with Swedbank.
- Ecommerce: Add support for new EveryPay payment methods: `medicinos`, `revolut`, `siauliu`.
- Ecommerce: Do not allow checking out a cart if a non-applicable discount code is in use.

## 2023-03-22

- Ecommerce: Add support for updating more order attributes via the [Orders API](https://www.voog.com/developers/api/ecommerce/orders#update_order).
- Ecommerce: Show shipment tracking code in the order details admin view.
- Ecommerce: Fix error when modifying the VAT code field in checkout settings admin view.

## 2023-03-20

- Ecommerce: Improve UX of products' and orders' bulk editors.
- Ecommerce: Add support for environment-specific delivery provider credentials in shipping settings admin view.
- Ecommerce: Fix a regression in checkout preview.
- Ecommerce: Fix issue where order contents were displayed in the wrong language in checkout result.

## 2023-03-08

- Prevent form submission when form is removed from page.
- Ecommerce: Fix admin fonts fallback when user has required fonts installed.
- Ecommerce: Improve order presentation in order details admin view.
- Ecommerce: Enhance UX for system fields in checkout settings admin view.

## 2023-03-01

- Ecommerce: Send order data to enabled delivery provider automatically after successful payment.
- Ecommerce: Indicate orders with package labels in the orders listing admin view.

## 2023-02-24

- Ecommerce: Fix consigning orders to Omniva.

## 2023-02-21

- Ecommerce: Improve delivery configuration UX in the shipping settings admin view.

## 2023-02-17

- Ecommerce: Introduce exporting package labels in bulk to the orders listing admin view.

## 2023-02-16

- API: Support downloading package labels in bulk via [Orders API](https://www.voog.com/developers/api/ecommerce/orders#download_invoices).
- Ecommerce: Fix displaying SVG product images in checkout.
- Ecommerce: Display product name in the expected language in the on-site shopping cart after adding it from the product list content area.

## 2023-02-13

- Ecommerce: Do not display the discount row in the order details admin view if a discount code has been entered, but no discount applies.

## 2023-02-10

* Ecommerce: Add delivery provider integration for Itella Smartpost.
* Ecommerce: Add Latvian and Lithuanian parcel machine list support to Itella Smatpost.
* Ecommerce: Add PDF invoice bulk download support to the orders listing admin view.
* Ecommerce: The export of products and orders takes into account bulk selections.
* Ecommerce: Update credit card logos.

## 2023-02-08

* API: Add PDF invoice bulk download support to the [Orders API](https://www.voog.com/developers/api/ecommerce/orders#download_invoices).

## 2023-02-06

* Ecommerce: Refine the user experience of orders' admin views.
* Ecommerce: Add bulk update capabilities to the orders listing admin view.

## 2023-02-01

* API: Introduce the [Delivery Provider Configurations](https://www.voog.com/developers/api/ecommerce/delivery_provider_configurations) and [Shipments APIs](https://www.voog.com/developers/api/ecommerce/shipments) for integrating orders with delivery providers, including PDF package label queries.
* Ecommerce: Add configuring delivery provider integrations to the shipping settings admin view.
* Ecommerce: Add delivery provider integrations for Omniva.
* Ecommerce: Enable printing package labels in the order details admin view for orders whose shipping method is integrated with a delivery provider.

## 2023-01-26

* Fix a bug where external link menu entries would not allow the `!` character in their URLs.
* Signup: Resolve an error that prevented completing the sign-up in Firefox Strict mode.
* API: Add bulk update capabilities to the [Orders API](https://www.voog.com/developers/api/ecommerce/orders#bulk_update_orders).
* API / Liquid: Enable filtering articles by tag (using the `q.tag.X` [query filter](https://www.voog.com/developers/api/basics/filters) syntax) for the [Articles API](https://www.voog.com/developers/api/resources/articles#filter) and the [load](https://www.voog.com/developers/markup/tags/load) tag.

## 2023-01-18

* Ecommerce: Fix a bug where updating a product via its buy button could overwrite its translations.

## 2023-01-16

* Ecommerce: Various enhancements to orders' admin views.

## 2023-01-10

* Ecommerce: Improve translating categories in the product details admin view.


## 2023-01-04

* Ecommerce: Address various regressions in orders' admin views.
* Ecommerce: Resolve an error that prevented checkout completion when all shipping methods were disabled.


## 2022-12-27

* Ecommerce: Introduce a redesigned orders listing admin view.
* Ecommerce: Implement translating categories in the product details admin view.

## 2022-12-21

* Fix a bug in the site verification view.

## 2022-12-20

* Introduce a redesigned sign-up view.
* Ecommerce: Fix untranslated shipping methods in checkout.

## 2022-12-15

* Ecommerce: Enhance products listing admin view's bulk update interface.


## 2022-12-14

* API: Add [bulk update](https://www.voog.com/developers/api/ecommerce/products#bulk_update_products) and [bulk delete](https://www.voog.com/developers/api/ecommerce/products#bulk_delete_products) support to Products API.
* Ecommerce: Implement bulk update and bulk delete in the products listing admin view.

## 2022-12-07

* Ecommerce: Add a dialog for translating products and their variants to the product details admin view.
* Ecommerce: Add presets with predefined delivery methods to the shipping settings admin view.

## 2022-12-01

* Display a one-time confirmation dialog in map content areas before loading Google Maps to ensure GDPR compliance.

## 2022-11-30

* Ecommerce: Introduce the redesigned shipping settings admin view.
* Ecommerce: Allow reordering variant types and variant values in the product details admin view.
* Ecommerce: Fix error on saving Swedbank payment gateway settings.
* Fix asset URLs in exported site snapshot.

## 2022-11-24

* Ecommerce: Show number of available products upon receiving a quantity exceeded error in the shopping cart.
* Ecommerce: Save product variant types and display the resulting variants immediately on editing a variant type in the product details admin view.
* Optimize JS bundles.

## 2022-11-17

* Ecommerce: Improve discount code visibility in checkout flow.
* Ecommerce: Product management admin view improvements

## 2022-11-16

* Voog subscriptions: Show Apple Pay logo in checkout.
* General security improvements.

## 2022-11-09

* Fix error when the front page of unknown language is requested.

## 2022-11-02

* Fix restoring layout assets in the design editor.
* Add price hike notification to the plans admin view.

## 2022-10-30

* Add a global price hike notification banner.

## 2022-10-28

* Ecommerce: Add the catalogue layout to the product list content area.
* Ecommerce: Fix canonical product pages returning a HTTP/404 error if the front page type is "blog" or "elements".
* Ecommerce: Fix regression where the maximum number of decimal places after the separator was 2 instead of 4 in product and product variant prices.
* Ecommerce: Clarify help text for the option to disable buy buttons in store settings admin view.
* Ecommerce: Do not allow an invalid currency code in store settings admin view.
* Voog subscriptions: Always send an e-mail to the customer if PDF invoice has been selected as the payment option.
* Refine the help menu.

## 2022-10-20

* Ecommerce: Add the masonry layout to the product list content area.
* Ecommerce: Change copy of customer notification e-mails to not assume physical products.
* Voog subscriptions: Add Apple Pay support.

## 2022-10-19

* Ecommerce: Fix bug where the checkout summary and order details admin view failed to load if a custom checkout field had not been filled in by the customer.
* Preserve selected text when dragging and dropping a file into the text editor.

## 2022-10-13

* Add Lithuanian support for end users ([Liquid translations](https://www.voog.com/developers/markup/basics/i18n), forms, cart, checkout, Ecommerce customer e-mails).
* Add search by domain name to the dashboard.
* Ecommerce: Implement navigating to the previous or next product in the product settings admin view.
* Ecommerce: Restore displaying the number of booked products and variants in product settings admin view.
* Ecommerce: Fix error where changing the product's status reset changes to other fields in product settings admin view.
* Ecommerce: Fix tax amount calculation in orders' export formats in the case where product and shipping tax rates differ.
* Liquid: Fix the [customstyle](https://www.voog.com/developers/markup/tags/customstyle) tag to only allow valid CSS variables (starting with `--`).

## 2022-09-29

* Ecommerce: Remember the number of items per page in product management admin view.
* Improve keyboard accessibility by allowing modal and semi-modal dialogs to be closed by pressing the Escape key.

## 2022-09-21

* Ecommerce: Introduce bulk management of product variants.
* Ecommerce: Improve product management admin view UX.
* Ecommerce: Fix product variants' price range calculation.
* Improve design customization flow.
* Fix buttons of semi-modal dialogs to the bottom of the screen on wide viewports.

## 2022-09-15

* Allow manually refreshing a Let's Encrypt SSL certificate 7 days before expiration.
* Ecommerce: Improve product management admin view UX.

## 2022-09-06

* Create link with the file name on dragging and dropping a file into the text editor.
* Improve Let's Encrypt certificate renewal process.

## 2022-08-31

* Ecommerce: Fix category handling in product settings admin view.

## 2022-08-31

* Fix gallery lightbox displaying low-quality images on zoom.
* Show warning in edit mode if page is redirected.
* Fix month selection in date pickers.
* Add a pay by link option to the offline payment e-mail when updating Voog subscription plan.

## 2022-08-29

* Add Google [reCAPTCHA v3](https://developers.google.com/recaptcha) support for article comments (enabled by default).
* API: Add the `recaptcha` flag to [Articles API](https://www.voog.com/developers/api/resources/articles#create_article).
* API: Add the `g-recaptcha-response` parameter to [Comments API](https://www.voog.com/developers/api/resources/comments#create_comment).
* Ecommerce: Improve product management admin view UX.
* Liquid: Add new [translation keys](https://www.voog.com/developers/markup/basics/i18n) for the [lc](https://www.voog.com/developers/markup/basics/filters#lc) filter.
* Improve domain redirect loop detection.

## 2022-08-25

* Ecommerce: Fix handling of Swedbank payment gateway notifications.

## 2022-08-18

* Change password protected page user invitation e-mail copy.
* Support IDN e-mails in the login form.
* Block some additional malicious bots in default `robots.txt`.

## 2022-08-09

* Ecommerce: Improve product management admin view UX.
* Fix page and article settings OG image picker for mobile devices.

## 2022-07-28

* Ecommerce: Introduce the new products management admin view.

## 2022-07-01

* Introduce the new login view.
* Ecommerce: Add [category based discounts](https://www.voog.com/support/online-store/discount-codes) ([Discounts API](https://www.voog.com/developers/api/ecommerce/discounts)).

## 2022-06-22

* Ecommerce: Always allow public access to canonical product page when store is enabled.
* API: Fix missing language context in Categories API cache.
* Add new onboarding wizard to the help menu.
* Improve category selection in product list content area settings.
* Fix `.org` domain lookup when buying a domain.
* Fix code editor file drop error handling.
* Display two digits after decimal point in referral earnings view.

## 2022-06-15

* Add targeting classes to form content area checkbox (`form_field_checkbox_label`) and radio button (`form_field_radio_label`) labels.
* Improve Spotify URL handling in [social media content area](https://www.voog.com/support/content-areas/what-is-a-content-area).

## 2022-06-07

* Improve input fields' behavior.
* Remove data usage bar from assets view when account's quota is unlimited.

## 2022-06-03

* General code improvements.

## 2022-06-01

* Add the [Voog Plus MakeCommerce special plan](https://www.voog.com/makecommerce).
* Remove the `data-title` attribute from a gallery thumbnail if it is not present.
* Fix date picker rendering on small viewports.

## 2022-05-26

* Fix redirect lookup when the request path ends with a slash.
* Fixed `editable` `product.description` change detection on saving.

## 2022-05-19

* Fix browser history handling within SEO views.
* Add TikTok to social media [content area](https://www.voog.com/support/content-areas/what-is-a-content-area).

## 2022-05-09

* Offer the [redirect feature](https://www.voog.com/support/seo/seo-optimization-in-voog) on the [Voog Plus](https://www.voog.com/pricing) plan.
* Ecommerce: Sync on-site shopping cart data between browser tabs.

## 2022-05-03

* Ecommerce: Fix a bug where attempting to check out a cart with nonexistent products failed silently.
* Ecommerce: Add new payment methods to the [EveryPay payment gateway](https://www.voog.com/support/online-store/everypay-bank-links) (`coop`, `luminor`).
* Liquid: Add the `title` and `title_tooltip` attributes to the [content ](https://www.voog.com/developers/markup/tags/content) tag.
* Liquid: Add new [localization keys](https://www.voog.com/developers/markup/basics/i18n) for the `lc` filter.
* Liquid: Add the `og_image` and `og_image?` properties to the [article](https://www.voog.com/developers/markup/objects/article#article_og_image), [menuitem](https://www.voog.com/developers/markup/objects/menu-item#menuitem_og_image), [page](https://www.voog.com/developers/markup/objects/page#page_og_image) and [product](https://www.voog.com/developers/markup/ecommerce-objects/product#product_og_image) objects.

## 2022-04-19

* Fix slider gallery animations flickering on Safari.

## 2022-04-11

* Ecommerce: Add new payment methods to the [Montonio payment gateway](https://www.voog.com/support/online-store/montonio-bank-links) (`revolut`, `danske`, `alandsbanken`, `handelsbanken`, `omasaastopankki`, `poppankki`, `saastopankki`, `spankki`).

## 2022-04-06

* Liquid: Allow the `@` symbol in the [menulink](https://www.voog.com/developers/markup/tags/menulink) tag.
* Improve menu items' reordering in mobile views.

## 2022-03-31

* Liquid: Do not escape `content single="text"` [content](https://www.voog.com/developers/markup/tags/content#single) output by default.

## 2022-03-29

* Improve .ee domain registration process.

## 2022-03-24

* Ecommerce: Add [Swedbank payment gateway](https://www.voog.com/support/online-store/swedbank-payment-gateway).
* Ecommerce: Don't display the product filter if there are no items in a product list content area.
* Ecommerce: Fix a bug where the checkout flow became stuck if a time input field was used.

## 2022-03-23

* Ecommerce: Add mobile layout options for product list content area's grid view.
* Ecommerce: Fix product list content area's effective locale in edit mode.

## 2022-03-21

* Ecommerce: Support deleting a product via the product list content area.
* Ecommerce: Fix the "New product" link in the product list content area.
* Ecommerce: Improve filtering for [Products API](https://www.voog.com/developers/api/ecommerce/products) export formats.
* Internal on-site search now respects the [`robots`](https://developers.google.com/search/docs/advanced/robots/robots_meta_tag) meta tag and page's / site's "Visible to search engines" settings.

## 2022-03-15

* Ecommerce: Set product list content area's default sort order to newest first.
* Fix redirection after successful login to a password protected page.

## 2022-03-10

* Designs: Improve auto-generated product pages in stock designs.

## 2022-03-07

* Ecommerce: Add filtering by category to product list admin view.
* Ecommerce: Add product filtering to the product list content area.

## 2022-03-02

* Ecommerce: Generate product slug translations from name by default.
* Ecommerce: Fix store mountpoint path caching.
* Liquid: Improve [image tag](https://www.voog.com/developers/markup/tags/image)'s `sizes` attribute.

## 2022-02-18

* Promote the new product list content area in the add content area dialog.
* Liquid: Fix regression where content block without a default value (`{% contentblock %}{% endcontentblock %}`) was not rendered.

## 2022-02-17

* API: Fix a bug when filtering by secondary objects: the filter now only applies to the primary objects, but the secondary objects are left as are.
* Ecommerce: Fix a bug where only the first 50 categories were displayed in product admin view and product list content area settings.
* Ecommerce: Add out of stock labels to the product list content area.
* Ecommerce: Fix URL routing for forms bound to canonical product pages.
* Ecommerce: Improve description rendering in product list content area.
* Liquid: Add the [truncate_html](https://www.voog.com/developers/markup/basics/filters#truncate_html) filter.
* Liquid: Add the [where](https://www.voog.com/developers/markup/basics/filters#where) filter.
* Liquid: Add the [at_least](https://www.voog.com/developers/markup/basics/filters#at_least) filter.
* Liquid: Add the [at_most](https://www.voog.com/developers/markup/basics/filters#at_most) filter.
* Designs: Auto-generated product page layout improvements in all [Voog standard designs](https://github.com/orgs/Voog/repositories?q=design).

## 2022-02-10

* Liquid: Add support for [sd_breadcrumbs](https://www.voog.com/developers/markup/tags/sd-breadcrumbs) to canonical product pages.
* Ecommerce: Clicking on the product image on a canonical product page in edit mode redirects to product admin view.
* Ecommerce: Fix content area rendering and relocating on canonical product pages.

## 2022-01-27

* Ecommerce: Add translatable URL slug support to products.
* Ecommerce: Support customizing store mount point (canonical product pages' root) in the site structure.
* Ecommerce: Support customizing the store slug (`/products/` by default) for the canonical product pages structure.
* Ecommerce: Support adding products via the product list content area.
* Ecommerce: Fix issue where rebuilding the product variant martrix was triggered unnecessarily.
* Ecommerce: Fix [webhook](https://www.voog.com/developers/api/ecommerce/webhooks) redirection handling.
* Ecommerce: Improve canonical product page's fallback design.
* Ecommerce: Make small enhancements to product list content area settings.
* Liquid: Add anchor tag class (`link-class`) support to the [menulink](https://www.voog.com/developers/markup/tags/menulink) tag.
* Liquid: Fix issue where variables where not evaluated in the [menulink](https://www.voog.com/developers/markup/tags/menulink) tag.
* Block some additional malicious bots in default robots.txt.
* Allow images in the `/photos/` directory to be indexed by crawlers by default.

## 2022-01-12

* API: Fix language context for [Products API](https://www.voog.com/developers/api/ecommerce/products) requests.
* Ecommerce: Display draft products in product list content area in edit mode.

## 2022-01-07

* Designs: Add design-specific canonical product page layouts (`content_type: "product"`) to all [Voog standard designs](https://github.com/orgs/Voog/repositories?q=design).

## 2022-01-07

* Ecommerce: Allow deleting a product even if it is bound to a buy button.
* Ecommerce: Improvements to canonical product page's buy button.

## 2021-12-31

* Ecommerce: Add the product count property to product list content area settings.
* Ecommerce: Add a direct link to the products admin view to product list content area settings.
* Ecommerce: Add the canonical product page to the Locations tab in product admin view.
* API: Improve sorting by translatable fields for [products](https://www.voog.com/developers/api/ecommerce/products) and [categories](https://www.voog.com/developers/api/ecommerce/categories).
* API: Support sorting by translatable fields in [Categories API](https://www.voog.com/developers/api/ecommerce/categories).

## 2021-12-23

* Ecommerce: Add sorting by creation date to product list content area.
* Ecommerce: Add categories to products list admin view and export files.
* Liquid: Add support for [Product](https://www.voog.com/developers/markup/ecommerce-objects/product)'s `title` and `description` fields to the [editable](https://www.voog.com/developers/markup/tags/editable) tag.
* Liquid: Add the [Category](https://www.voog.com/developers/markup/ecommerce-objects/category) object.
* Liquid: Add the `categories`, `created_at` and `updated_at` methods to the [Product](https://www.voog.com/developers/markup/ecommerce-objects/product) object.

## 2021-12-21

* Ecommerce: Add canonical product page layout support to design editor.
* Ecommerce: Do not display the column count selector in products content area settings if the list layout is selected.

## 2021-12-16

* Ecommerce: Add the product list content area (product widget).
* Ecommerce: Add category membership and the description field to the product object.
* Ecommerce: Improve the platform default (fallback) canonical product page layout.
* Ecommerce: Add the [Product Widgets API](https://www.voog.com/developers/api/resources/product_widgets).
* Ecommerce: Update the [Products API](https://www.voog.com/developers/api/ecommerce/products) to support description and category membership management.
* Liquid: Add the [Product list drop](https://www.voog.com/developers/markup/objects/product-widget).
* Liquid: Add the [image tag](https://www.voog.com/developers/markup/tags/image).
* Liquid: Add the [image_data tag](https://www.voog.com/developers/markup/tags/image-data).
* Liquid: Add the `schemeless_url` method to the [Asset drop](https://www.voog.com/developers/markup/objects/asset).
* Liquid: Add the `filename` method to the [Image drop](https://www.voog.com/developers/markup/objects/image).
* Liquid: Add the `product` and `url` methods to the [Product drop](https://www.voog.com/developers/markup/ecommerce-objects/product).
* Liquid: The [Language drop](https://www.voog.com/developers/markup/objects/language) works as expected in the context of canonical product pages.

## 2021-11-24

* Ecommerce: Add [Kniks gift card](https://kniks.ee/) support to the Makecommerce payment gateway.
* Ecommerce: Add the product [Categories API](https://www.voog.com/developers/api/ecommerce/categories).
* Fix signup with emails containing the `+` character.

## 2021-11-17

* Ecommerce: Improve store terms URL validation.
* Fix an unhandled exception in the catalog editor.
* Improve finding domains available for purchase.

## 2021-11-05

* Ecommerce: Support more currency symbols.
* Ecommerce: Inital support for auto-rendered canonical product pages. Introduce a new layout content type `product`.
* Liquid: Allow binding a [content area](https://www.voog.com/developers/markup/tags/content) to a [Product drop](https://www.voog.com/developers/markup/ecommerce-objects/product).
* Liquid: Add the [Variant type](https://www.voog.com/developers/markup/ecommerce-objects/product-variant-type) and [Variant value](https://www.voog.com/developers/markup/ecommerce-objects/product-variant-value) drops.
* Liquid: Add the `variant_values` method to the [Product drop](https://www.voog.com/developers/markup/ecommerce-objects/product), returning an array of [Variant types](https://www.voog.com/developers/markup/ecommerce-objects/product-variant-type).
* Liquid: Add the `title` method to the [Product drop](https://www.voog.com/developers/markup/ecommerce-objects/product)

## 2021-10-20

* API: Improve sorting performance over translated product fields in the [Ecommerce Products API](https://www.voog.com/developers/api/ecommerce/products).
* Sort product list by name after the previous performance improvement. 
* Ecommerce: Add a noticeable warning for if your store is disabled.
* General code improvements.

## 2021-10-12
* Ecommerce: Add a new default Checkout field: the company VAT code. Show it in Checkout views, e-mails, and the PDF invoice if present.
* Ecommerce: Add contract related warning for Montonio Split and financing.
* Send domain transfer code e-mail based on user locale.
* Send .ee registration e-mail based on user locale.
* General code improvements.

## 2021-10-04

* Ecommerce: Bypass the payment tab in the Checkout if the total amount of the cart is 0.
* Ecommerce: Display the product code in the order details and on the PDF invoice.
* Ecommerce: Allow navigation to products related to the order from the order details view.
* Ecommerce: Add the option to filter orders by customer name and e-mail.
* Ecommerce: Show product prices in the admin view of the product list.
* Ecommerce: Improve existing product lookup selection for the buy button modal.
* Ecommerce: Disallow to archive unprocessed orders (with payment statuses "unpaid" or "pending").
* Ecommerce: Add IDN support to store reply and notification e-mails.
* Block bad crawlers in the site's default `robots.txt`.

## 2021-09-20

* Ecommerce: Add [Montonio Split](https://montonio.com/et/montonio-split-tapselt-oige-tasakaal-valjaostu-ja-jarelmaksu-vahel/) support.
* Ecommerce: Improve the rendering of the product editing form for currency codes unknown to the CMS.
* Improve the performance of rendering edit mode requests.
* Improve the accessibility of the support chat in mobile view.

## 2021-09-08

* New: Add [Spanish langage](https://www.voog.com/developers/markup/basics/i18n) support for the website's public interface (Liquid templates, Checkout, Ecommerce customer-related e-mails).
* Ecommerce: Update PayPal's setup instructions.

## 2021-08-31

* Ecommerce: Fix an issue where the browser autofill function sometimes breaks the checkout flow in the Checkout.

## 2021-08-26

* Update the Voog domains [price list](https://www.voog.com/support/your-website-addresses/domain-prices).

## 2021-08-09

* Ecommerce: Update the VISA logo to match their new [brand](https://merchantsignageeu.visa.com/product.asp?dptID=696).

## 2021-08-03

* API: Update the [Ecommerce Order API](https://www.voog.com/developers/markup/ecommerce-objects/order) documentation.
* Ecommerce: Fix product image rendering in the on-site shopping cart when the image's file name contains special characters.

## 2021-07-02

* API: Update the [Ecommerce Gateways API](https://www.voog.com/developers/api/ecommerce/gateways) documentation.
* API: Update the [Assets API](https://www.voog.com/developers/api/resources/assets) documentation. Add a description of the uploading process.
* Improve the performance of destroying objects.

## 2021-06-28

* Change: Images are now processed asynchronously during upload.
* API: Add new asset "status" to [Assets API](https://www.voog.com/developers/api/resources/assets).
* Ecommerce: Display credit-based payment methods in a separate section in the Checkout.

## 2021-06-20

* Ecommerce: Add [Montonio](https://montonio.com/) payment gateway support.
* Ecommerce: Add the Ecommerce [Templates API](https://www.voog.com/developers/api/ecommerce/templates). Read more about the [customization of the PDF invoice and customer e-mails](https://www.voog.com/developers/markup/basic-examples/ecommerce-templates) in Voog Ecommerce.
* Liquid: Add documentation for Liquid objects related to the [Ecommerce templates](https://www.voog.com/developers/markup/ecommerce-objects). 

## 2021-06-15

* Ecommerce: Display gross shipping amount in the Checkout's shipping tab.
* Fix galleries displaying low-quality thumbnails in some cases.

## 2021-06-03

* Ecommerce: New on-site shopping cart dialog (for v2).
* Ecommerce: Fix monetary amount rendering for 3-character currency codes in Liquid.
* Ecommerce: Allow clearing discount validity date fields.

## 2021-05-27

* Ecommerce: Create preview capability for customized shopping cart fields.
* Ecommerce: Add keyboard navigation to checkout settings and improve focus handling.
* Ecommerce: Fix product reservation logic on status change.
* Ecommerce: Fix UX bugs in checkout v2.

## 2021-05-19

* Ecommerce: Enhance checkout fields customization interface.
* Ecommerce: Display used discount code in admin e-mails.
* Ecommerce: Fix bug where product's min and max prices were not updated on price change.
* Ecommerce: Show price on buy button if all variants have the same price.

## 2021-05-04

* Ecommerce: Add admin interface for customizing checkout (v2) fields.
* Ecommerce: Improve checkout locale handling.
* Improve assets database indexing.

## 2021-04-23

* Ecommerce: Fix UX bugs in checkout v2.

## 2021-04-20

* Liquid: Add cart related [localization keys](https://www.voog.com/developers/markup/basics/i18n) for the `lc` tag.
* Ecommerce: Fix bug where shipping method names were not translated in checkout.

## 2021-04-19

* Ecommerce: Add custom fields support to checkout. Configuration is available via [Cart fields API](https://www.voog.com/developers/api/ecommerce/cart_fields).
* Ecommerce: Fix order creation webhooks failing if the order contains a product with an image.
* Ecommerce: Deny possible HTML and JS injection to PDF invoice.
* Remove client's IP address from form tickets and article comments.

## 2021-04-07

* Liquid: Improve menu loading time.

## 2021-04-01

* Add site verification support. A new website is unavailable to the public until site owner verifies it by email.

## 2021-03-29

* Ecommerce: Fix checkout tablet view UI issues.
* Ecommerce: Amend payment instructions with recipient and description in checkout return view.
* Ecommerce: Switch shipping and billing address titles in detailed order view.
* Ecommerce: Defer duplicating shipping address from billing address until final order checkout.
* Add alt text to wall and slider gallery thumbnails.

## 2021-03-18

* Ecommerce: Apply domain iframe settings to checkout.

## 2021-03-10

* Ecommerce: Set shipping address to selected pick-up point's address, if applicable.
* Ecommerce: Do not display 0% tax rate row in e-mails.

## 2021-03-05

* Ecommerce: Do not display 0% tax rate row in checkout.

## 2021-02-22

* Fix HTTP/301 redirect rules for language front pages.

## 2021-02-10
* Ecommerce: Add events support to Checkout v2. [Read more](https://www.voog.com/developers/scripting/checkout-flow-v2).
* Ecommerce: Add product image URL to the CSV and XLS outputs.


## 2021-02-09
* Designs: Initial release of [Nuuk ](https://github.com/Voog/design-nuuk). [See here](https://nuuk.voog.com/) for a demo site.

## 2021-02-09
* Harmonize heading names in the text editor and the design editor. Add the H4 style.
* Liquid: Add new attributes to the [menuadd tag](https://www.voog.com/developers/markup/tags/menuadd): `title`, `label`, `layout_title`, `style`, `class`.
* Liquid: Add [new keys](https://www.voog.com/developers/markup/basics/i18n) for the `lc` and `lce` filters.
* Ecommerce: Introduce dedicated tablet design for Checkout v2.

## 2021-02-01
* Ecommerce: Fix sending of stock warning and webhook error notification e-mails.

## 2021-01-27
* Ecommerce: Add product image support to the admin interface.
* Ecommerce: Fixes and improvements to checkout flow v2.
* Ecommerce: Dispatch the `voog:ecommerce:buttonproductsave` event when [buy button](https://www.voog.com/developers/scripting/ecommerce/buy-buttons-manager) settings are saved.
* Ecommerce: Improve PDF invoice rendering when store's tax rate is zero.
* Ecommerce: Use store name in customer e-mails' From field.
* Liquid: Fix `available?` method in the [BuyButton drop](https://www.voog.com/developers/markup/objects/buy-button).
* Liquid: Fix rendering product JSON.
* Liquid: Fix rendering translated product names.

## 2021-01-13
* Ecommerce: Retain orders and products filter state in the respective admin views.
* Optimize animated GIF thumbnail generation.

## 2020-12-31
* Introduce HTTP/2 support.

## 2020-12-17
* Ecommerce: Introduce support for product images.
* API: Add `image`, `image_id`, `price_min` and `price_max` fields to the [Products API](https://www.voog.com/developers/api/ecommerce/products).
* API: Add the `image` field to product entries in [Carts ](https://www.voog.com/developers/api/ecommerce/carts) and [Orders](https://www.voog.com/developers/api/ecommerce/orders) APIs.
* Liquid: Add `image`, `image?`, `price_min`, `price_max`, `price_min_with_tax`,  `price_max_with_tax` and `currency` to the [Product drop](https://www.voog.com/developers/markup/objects/product).
* Liquid: Add `thumbnail` to the [Image drop](https://www.voog.com/developers/markup/objects/image)

## 2020-12-17
* Ecommerce: Introduce the new checkout flow (v2, default for new stores).
* Ecommerce: Improve invoice PDF layout for long content.
* Fix grid galley thumbnail size calculation.

## 2020-12-09
* Support `youtube-nocookie.com` as an embedded video URL.

## 2020-12-09
* Ecommerce: Fix a bug in order status e-mails in case a related discount has been deleted.

## 2020-11-17
* Add extra information and sorting functionality to the SEO Pages view.
* API: Add `customer.language` to Ecommerce [Orders API](https://www.voog.com/developers/api/ecommerce/orders) response.
* Ecommerce: Fix preview text rendering in customer e-mails.

## 2020-11-17
* Use site domain for page and article OG image URLs.

## 2020-11-05
* Display 250 entries in SEO Pages view.
* Update domain price list.

## 2020-10-15
* Update subjects and preview texts of e-mails sent to the site owner.

## 2020-10-09
* Support 4-byte UTF-8 characters (emojis) in content area, article excerpt and body, and element data columns (`text` data type). 4-byte UTF-8 characters are now converted to HTML entities upon save.

## 2020-10-08
* Performance: Change `Element` and `ElementDefinition` backing data storage and serialization format to improve processing time.
* General code and copy improvements.

## 2020-10-07
* Ecommerce: Liquid Drop improvements.
* Ecommerce: Send e-mails asynchronously.
* Performance: Reduce size of downloaded JS bundles and improve loading logic for better parallelization.
* General code and copy improvements.

## 2020-09-16
* Update design of Voog e-mails.

## 2020-09-08
* Fix wrong currency code in transaction fee report.

## 2020-09-02
* Ecommerce: Add `luminor` payment method to EveryPay gateway.
* Fix product variants settings menu style.

## 2020-08-31
* Ecommerce: Add [EveryPay](https://every-pay.com/) payment gateway support.

## 2020-08-27
* Ecommerce: Add e-mail and PDF invoice previews to store settings.
* Ecommerce: Add support for new Stripe Checkout [payment methods](https://stripe.com/docs/payments/checkout/payment-methods) –
  * Alipay (China - AUD, CAD, EUR, GBP, HKD, JPY, NZD, SGD, USD, MYR)
  * Bancontact (Belgium - EUR)
  * Giropay (Germany - EUR)
  * EPS (Austria - EUR)
  * Bacs Direct Debit (UK - GBP)
  * Przelewy24 (Poland - EUR, PLN)
  * FPX (Malaysia - MYR)

## 2020-08-12
* Fix a visual bug in DNS settings view.
* Improve UI tooltips.
* Ecommerce: Support customizable customer e-mails and PDF invoices (alpha version – by request only).

## 2020-08-06
* New look for Voog onboarding e-mails.

## 2020-08-03
* Ecommerce: Fix shipping method option validation on cart update and checkout.

## 2020-06-29
* Ecommerce: Integrate delivery providers - auto-updated pick up point and parcel terminal lists for DPD, Itella Smartpost and Omniva.
* API: Add the `delivery_method` data structure to [Shipping methods API](https://www.voog.com/developers/api/ecommerce/shipping_methods), representing the integrated delivery provider associated with the shipping method.

## 2020-06-16
* Ecommerce: Reflect shopping cart rule discounts in e-mails.

## 2020-06-14
* Add [Google reCAPTCHA v3](https://developers.google.com/recaptcha) support for forms (enabled by default).
* API: Add the `recaptcha` flag to [Forms API](https://www.voog.com/developers/api/resources/forms).

## 2020-06-03
* Ecommerce: Refresh shopping cart on review.

## 2020-06-01

* Ecommerce: Use different color if the order status is unpaid or not_dispatched.
* Liquid: Fixed [contentblock](https://www.voog.com/developers/markup/tags/contentblock#publish_default_content) regression where `publish_default_content` value was ignored.

## 2020-05-28

* Liquid: Added `buy_button` and `buy_buttons` support to the [`load`](https://www.voog.com/developers/markup/tags/load) tag.
* Liquid: Added the [buy_button](https://www.voog.com/developers/markup/objects/buy-button), [content](https://www.voog.com/developers/markup/objects/content) and [product](https://www.voog.com/developers/markup/objects/product) objects.
* Ecommerce: Fixed Luminor logos in shopping carts for the LT and LV regions.
* Ecommerce: Support dynamic shipping pricing (e.g. free shipping or reduced shipping cost for orders over a given total amount).
* API: Added Ecommerce [Cart rules API](https://www.voog.com/developers/api/ecommerce/cart_rules).

## 2020-05-25

* Ecommerce: Show separate payment and shipping statuses in orders view.
* Ecommerce: Added [Luminor E-Commerce payment gateway](https://www.luminor.ee/en/business/luminors-e-commerce-gateway).

## 2020-05-13

* Ecommerce: Updated payment method logos
* Ecommerce: Added notification language option to store settings and [Store settings API](https://www.voog.com/developers/api/ecommerce/store_settings).
* Ecommerce: Send store admin e-mails in notification language

## 2020-05-11

* Ecommerce: Clean stale cache on discount object update.
* General code and copy improvements.

## 2020-05-08

* Ecommerce: Added [Stripe payment gateway](https://stripe.com/checkout) support. Stripe supports Apple Pay and Google Pay out of the box.
* Show a label next to form tickets marked as spam.

## 2020-05-07

* Ecommerce API: Added the [Webhooks API](https://www.voog.com/developers/api/ecommerce/webhooks). Supported object: `order`. Supported events: `create`, `update` and `delete`. [Read more](https://www.voog.com/developers/api/ecommerce/webhooks).
* Added the `form_submit_input` class to form submit buttons.
* Retain image format when generating thumbnails. Previously the `medium` size was always saved as JPEG.
* General code and system improvements.

## 2020-05-04

* Ecommerce: Improved payment gateway notification processing and retry stability.

## 2020-04-28

* Password protected pages invitation emails are sent out in the page language instead of the inviting user's language, if the language is supported.
* Ecommerce: Keep product information attached to buy buttons on page duplication.
* General code and system improvements.

## 2020-04-27

* Ecommerce: Fixed a bug related to updating shipping methods.

## 2020-04-20

* Ecommerce: Store and show the external gateway transactio ID as `gateway_transaction_id` field in [Orders API](https://www.voog.com/developers/api/ecommerce/orders) response.

## 2020-04-16

* Ecommerce: Support translatable shipping methods (`name` and `description` fields).

## 2020-04-15

* Ecommerce: Fixed shopping cart views and totals calculation if `Voog.ShoppingCart.showCart` is invoked externally.
* Ecommerce: Added the `language_id` field to the `page` object of [Elements API](https://www.voog.com/developers/api/resources/elements) response.
* Ecommerce: Added the `sku` and `parent_id` fields to the `product` object of [Orders API](https://www.voog.com/developers/api/ecommerce/orders) response.

## 2020-04-13

* Use the `email` input type for e-mail fields in the form content area.
* Ecommerce: Fixed cart totals calculation.

## 2020-04-09

* Fixed saving boolean flags in domain settings.
* Ecommerce: Improved buy button rendering in edit mode.
* Ecommerce: Separated payment and shipping statuses in order filtering.
* Ecommerce: Show quantity of a product in order details mobile view.
* Ecommerce: Add more tooltips to store settings.

## 2020-04-04

* Ecommerce: Added support for minimum cart amount requirement.
* Ecommerce: Added capability to make buy buttons publicly unavailable (pause shopping).
* Ecommerce: Fixed order notification e-mail reply-to addresses. Use customer's e-mail in notifications to the shop owner and shop e-mail in notifications to the customer.
* Ecommerce: Enabled `terms_agreement_required` flag by default on new store creation.
* Ecommerce: Show 50 records per page in orders and products views.
* Ecommerce: Added tooltip to discount amount field.
* Ecommerce: Allow up to 1 MB of text in the shipping method options field.
* Ecommerce API: Added `is_publicly_unavailable` and `min_cart_total` to [Store Settings API](https://www.voog.com/developers/api/ecommerce/store_settings).

## 2020-03-27

* Fixed asset collection list ordering in file picker toolbar.

## 2020-03-26

* Redesigned the file picker toolbar.
* Fixed chat icon positioning in admin catalog view.

## 2020-03-23

* API: Fixed article draft / publishing / published status update logic.
* API: Fixed Elements and Articles authorization - elements and articles of password protected pages are now readable and updatable.
* Fixed issue where [plain text content](https://www.voog.com/developers/markup/tags/content#single) was converted to rich text on page duplication.

## 2020-03-13

* Improved auto-SSL features.

## 2020-03-11

* Ecommerce: Shopping cart data are now stored in browser `localStorage`.
* Ecommerce: Improved buy button performance when selecting an existing product.
* API: Allow deletion of restricted API objects (i.e. features not enabled in the current subscription plan).
* General code and system improvements.

## 2020-03-05

* General code and system improvements.

## 2020-02-26

* Fixed page reload and redirection on page update and delete via the semi-modal dialog.
* Automatically provision Let's Encrypt SSL certificates for newly added domains (sites with stock designs only).
* Force SSL for domains with recently activated certificates (sites with stock designs only).
* General code and system improvements.

## 2020-02-03

* Added a separate help menu to Dashboard
* Fixed broken "+" button in toolbar menus (blog, user, site)
* Various Dashboard and toolbar fixes
* Changed HTML editor and trashcan positioning in line with the new toolbar

## 2020-01-29

* Introduced the main menu redesign
* Improved Dashboard loading and UI
* Set Dashboard as the post-login landing page
* Fixed a restored page not re-appearing in SEO Pages listing
* Voog support chat is now also visible off-hours
* API: Fixed Products API for the case when all site languages have been deleted
* API: Do not include the `locations` section to Products API responses to anonymous requests
* API: Improved Ecommerce API documentation about [anonymous endpoints](https://www.voog.com/developers/api#anonymous_access)
* Ecommerce: Fixed status update for orders in paginated views
* General code and system improvements

## 2020-01-07

* Added a link to SEO admin views to Dashboard

## 2019-12-20

* Introduced a new Dashboard view

## 2019-12-12

* Added a new application server node

## 2019-11-29

* Reduced site structure management view reloads
* Fixed adding a buy button for editors in Standard and Plus plans
* General code and system improvements

## 2019-11-20

* Improved Let's Encrypt SSL certificates management and stability
* Improved loading semi-modal dialogs
* Fixed page deletion flash messages
* General code and system improvements

## 2019-11-12

* Fixed and improved UX/UI of SEO admin views
* API: Fixed HTTP/500 response in Pages API when a link-type page received `null` for `layout_id`
* Reduced JS bundle sizes
* General code and system improvements

## 2019-11-06

* Added redesigned article settings dialog
* Added redesigned elements settings dialog
* Ecommerce: Support additional MakeCommerce payment methods (Finora, Slice and mTasku)
* Support older browsers without Shadow DOM support (e.g. IE11)
* Improved content draghandler

## 2019-10-10

* Made content area toolbar z-index higher than overlay and its popover
* Fixed page OG image removal
* Updated recurring payment period copy in subscriptions view
* Ecommerce: Send weekly transactions report e-mail to shop owners (shops with a transaction fee only)
* General code and system improvements

## 2019-10-03

* Migrated client-facing map widgets to Google Embed API
* Fixed saving site title in SEO General view
* Fixed content area manipulation UI z-indices

## 2019-10-01

* Fixed issue where the page settings dialog always displayed "public" as password protected state
* Fixed image picker for file names with special characters

## 2019-09-27

* New and improved image picker for OG image in the page settings dialog
* Fixed bugs in SEO dashboard views and improved performance
* Fixed SEO views for the case where all site languages are deleted
* Improved page and redirects settings modal dialogs
* Show subscription plan's recurring date in account plans view

## 2019-09-16

* Fixed: clean redirect rules cache on redirect rule change
* General improvements

## 2019-09-13

* Improved BuyButton rendering performance for products with variants

## 2019-09-12

* New SEO Redirect rules management view
* Added query string support for redirect rules (regex match only)
* Fixed FB icon click in social content area
* Improved SEO Pages upsell
* Added title formatting override tools to page settings dialog SEO tab
* General improvements

## 2019-09-09

* New password protected page user management popup in page settings dialog
* Added a descriptive label to page settings OG image input
* Improved content area management tools
* Ecommerce: Fixed email validation for long (> 3 chars) TLDs
* General improvements

## 2019-08-26

* Fixed form editor input activation in edit mode

## 2019-08-22

* Improved interactions of empty content area's "Add content" panel UI elements
* Fixed layout selector in the page settings dialog if there are more than 50 layouts
* Fixed private / public flag saving in page settings dialog
* API: Support `isprivate` as alias for `privacy` in Pages API
* General improvements

## 2019-08-16

* API: New Page API [duplicate endpoint](https://www.voog.com/developers/api/resources/pages#duplicate_page)
* Added page duplication to the new page settings dialog
* Fixed sub-page path renaming via Page API
* Fixed saving the Google Search Console field
* Fixed page URL in Google search result previews
* Fixed SEO General view's language context change
* Fixed issue where external CSS overrides "Add content area" button's design

## 2019-08-09

* Fixed "/robots.txt" endpoint regression

## 2019-08-05

* Fixed content area activating prematurely on hover
* Added delete confirmation to page settings dialog
* SEO tools: fixed arbitrary page's URL being displayed
* Improved content area styling
* General improvements

## 2019-07-31

* New SEO dashboard
* New redesigned page settings dialog
* Re-designed content area management
* API: Sitemap control via [Site API](https://www.voog.com/developers/api/resources/site)
* API: Support generic search for [Pages API](https://www.voog.com/developers/api/resources/pages) (`?search=somecontent`)
* Updated prices for the 2019 hike
* Added advanced redirect rules support
* Added [Redirect Rules API](https://www.voog.com/developers/api/resources/redirect_rules)

## 2019-07-04

* Add `menu_title` to the Page object. It's now possible to set a separate `page.menu_title` to display a different title in the menu, as opposed to the `<title>` tag. [`menuitem.title`](https://www.voog.com/developers/markup/objects/menu-item#menuitem_title) now returns `page.menu_title` when present, with fallback to `page.title`. The `menu_title` value can be updated over the [Page API](https://www.voog.com/developers/api/resources/pages).
* Support for `<title>` tag formatting (Site, Page and Article objects) used by the new [`title` Liquid tag](https://www.voog.com/developers/markup/tags/title). [`title_format`](https://www.voog.com/developers/markup/objects/page#page_title_format) and [`title_separator`](https://www.voog.com/developers/markup/objects/page#page_title_separator) values can be set over the API.
* Liquid: Add the [`title`](https://www.voog.com/developers/markup/tags/title) tag. Usage `<title>{% title %}</title>`. The tag uses Page / Article `title_format` and `title_separator` values with fallback to site level values (and system defaults). [Read more](https://www.voog.com/developers/markup/tags/title).
* Liquid: New fields for [Article](https://www.voog.com/developers/markup/objects/article): `full_title`, `title_separator`, `title_separator_value`, `title_format`, `title_format_pattern`.
* Liquid: New fields for [Page](https://www.voog.com/developers/markup/objects/page): `menu_title`, `full_title`, `title_separator`, `title_separator_value`, `title_format`, `title_format_pattern`.
* Liquid: New fields for [Site](https://www.voog.com/developers/markup/objects/site): `title_separator`, `title_separator_value`, `title_format`, `title_format_pattern`.
* API: Allow updating custom `robots.txt` content over the [Site API](https://www.voog.com/developers/api/resources/site).
* Support site level `robots_header` value. Can be set over the [Site API](https://www.voog.com/developers/api/resources/site). If set, any page level `robots_header` value is ignored.
* Add SEO metrics to [Pages](https://www.voog.com/developers/api/resources/pages) and [Articles](https://www.voog.com/developers/api/resources/articles) API-s.
* Preparation for August 1st release. [Read more in the blog](https://www.voog.com/blog/coming-soon-seo-tools-more-space-updated-subscription-plans).

## 2019-05-31

* Update TOS acceptances
* Include article image links in RSS feeds (`item.enclosure`)

## 2019-05-22

* Ecommerce: Fixed issue where stock notification email was sent too early
* General improvements

## 2019-05-10

* Fixed TOS acceptances modal rendering
* General improvements

## 2019-05-08

* Do not show "next" and "prev" buttons if slider has only 1 photo
* Liquid: Make `menuitem.page.description` accessible when menu items are loaded with the `_with_data` suffix 
* Improve UI/UX of invoices and subscriptions admin views
* General improvements in admin views

## 2019-04-09

* Add support for inline elements in [custom text format](https://www.voog.com/developers/scripting/page-configuration/adding-a-text-format)

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
