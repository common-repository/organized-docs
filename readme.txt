=== Organized Docs ===
Contributors: isabel104
Tags: documentation, docs, documentor, organized documentation, instruction guides, organized docs
Requires at least: 4.0
Tested up to: 5.5
Stable tag: 2.6.3
License: GNU Version 2
License URI: http://www.gnu.org/licenses/gpl-2.0.html

Create organized documentation for multiple products, organized by product and by subsections within each product.

== Description ==

Create documentation for any number of products, organized by product, and by sub-headings within each product. You can use this to create instruction guides for just about anything.

This is for you if any of these apply:

* You need to create software documentation.
* You need to create documentation for one or multiple products, and must have the docs organized neatly, by product. 
* You need to write instruction guides for virtually anything, whether it be products, games, topics, etc. You can label them as "Instructions" instead of "Docs".
* You don't want to create a separate website for your docs. You simply want to add them on to your current WordPress site.

This plugin organizes your documentation articles into a visitor-friendly, browse-able format that fits right into your WordPress site. This takes the headache out of organizing documentation articles and instruction guides.

**Built-in SEO**

Documentation articles will have schema.org microdata. It adds **TechArticle** microdata to single Docs, and **CollectionPage** microdata to Docs archives. You can disable the microdata.

**Documentation With a User-Friendly Structure For Your Visitors**

The main "Docs Page" will list all the products. Clicking on a product will take you to the docs only for that product.

Each product's docs are organized into subsections. The subsections list each individual article in that docs section. 

A single docs post will have a Table of Contents widget added to the sidebar. This will show a Table of Contents for docs pertaining only to the product which this current single doc belongs to. 

Organized Docs works on **Multisite** WordPress installations, as well as regular WordPress sites.

**To Consider**

This plugin focuses on 2 priorities: a user-friendly docs structure for your visitors, and fast, optimized pagespeed both on the front and back ends of your site (a very light footprint). So, we omit features that focus on backend ease and bloating. So, there is no drag-and-drop ordering of docs. This plugin uses categories to classify your docs rather than creating a whole new interface for docs.

[Quick Start Guide](https://isabelcastillo.com/docs/creating-docs)

For support, use the support forum link above.

== Installation ==

1.  In your WordPress dashboard, go to "Plugins -> Add New", and search for "organized docs".
2.  Click to install and then Activate the plugin.
3.  Create your Docs articles in your WordPress dashboard --> Docs --> Add New. See the [Quick Start Guide](https://isabelcastillo.com/docs/creating-docs) for more info.
4.  Add the main Docs page to your site's menu [with these steps](https://isabelcastillo.com/docs/how-to-add-docs-to-your-websites-menu).

== Frequently Asked Questions ==

= Why is the layout all messed up? = 

The Organized Docs layout is compatible with these default WordPress themes: Twenty Fifteen, Twenty Fourteen, Twenty Thirteen, and Twenty Twelve.

On other themes, the layout may look all messed up. You can fix this by copying the template files into your theme. Once you have copied them, make the necessary changes to the HTML to make it match your own theme, while leaving the important Organized Docs loop stuff intact.

See how to [Customize The Docs Template Files](https://isabelcastillo.com/docs/customize-the-docs-template-files).

== Screenshots ==

1. Main Docs page on 2015 theme showing all main, top-level items
2. All Docs for 1 product on 2015 theme
3. All Docs for 1 product on 2014 theme
4. All Docs for 1 product on 2013 theme
5. A single Docs article with Table of Contents on 2015 theme
6. A single Docs article with Table of Contents on 2014 theme
7. A single Docs article with Table of Contents on 2013 theme

== Changelog ==

= 2.6.3 =
* Fix - Some settings were not being saved.

= 2.6.2 =
* Fix - Only set meta_key arg if orderyby is = meta_value_num. Prematurely setting meta_key arg was causing the Table of Contents to be empty and missing navigation on docs posts if child categories were not set, and if the orderby for single docs was set to date or title. That is, this issue had only affected docs posts in which the single doc was attached to a top-level category without creating sub-categories (child categories), and if the 'orderby' setting for Single Docs was set to date or title. This was a very small, if any, number of use cases.

= 2.6.1 =
* Tweak - Improved CSS styles for single Docs.

= 2.6 =
* New - Update styles for Twenty Seventeen and Twenty Sixteen theme compatibility.
* New - Added up/down arrows to toggle headings, if toggle is enabled.
* New - Split settings page into tabs for less clutter.
* New - The "hide" option has been removed from the "List Each Single Title?" option for the "Top Level Category Pages" and for the Table of Contents widget. If you had either of those settings set to "hide," they have been now updated to "toggle".
* New - 2 template files have been changed: `taxonomy.php` and `single.php`. If you're using custom template files for Docs, you should update these to match the new ones.
* New - Removed action hook from the single.php template file: `organized_docs_single_after_nav`
* New - Changed widget name to Docs Table of Contents.
* New - Removed the "Publisher" item property since TechArticle structured data schema doesn't require it.
* New - Show orphan docs on archives and Table of Contens even if it's not assigned to child category (subheading) but is assigned directly to the parent category.
* New - Added support for subheadings links only for pages that have only 1 post for their top-level Docs category.
* Fix - Show "Setting Saved" message on the settings page when settings are updated.
* Tweak - Change #od-author to .od-author in the structured data meta tag so as not to create an extra microdata property id.

= 2.5.2 =
* Fix - Fixed improperly escaped author name.

= 2.5.1 =
* Tweak - remove duplicate .css file

= 2.5 =
* New - For Docs that only have 1 post for the top-level Docs category, there is a much improved display because there are cases where you only need 1 Doc page. (1) The main Docs page will link to the actual post, rather than linking to the category archive. (2) The Table of Contents sidebar for this post will not link to its own page; rather, it will show links that jump down to subheadings on the same page. (3) The redundant category heading will not be shown on this single Docs post, since there are no other posts in the category. Again, these 3 changes only apply to top-level Docs categories that have only 1 doc. See https://isabelcastillo.com/docs/jump-links
* Fix - Bettery alignment on docs archives pages. This is mainly a fix for Twenty Sixteen and Twenty Seventeen themes, but all full/wide width themes will have improved display.
* Fix - Fixed typo on the setting to disable comments.
* Tweak - textdomain should be loaded on the init action rather than on the plugins_loaded action.
* Tweak - Much escaping.
* Tweak - Moved the CSS file to the assets directory.
* Code refactor - The method name `Isa_Organized_Docs::register_style` was changed to `Isa_Organized_Docs::register_scripts`

= 2.4.2 2016-08-22 =
* Fix - Restore the missing option to Change The Main Docs Page Title.

= 2.4.1 =
* BREAKING CHANGE - Changed the filter named od_schema_author to od_author_name. If you are using that filter, you must update the name.
* New - Updated template single.php to just add a filter which you can use to display the author on single docs. See https://isabelcastillo.com/docs/display-author-single-docs
* Tweak - Add better CSS for single Docs post navigation links.

= 2.4 =
* New - No more automatically created menu item for "Docs." If you have not previously done so, you may want to add the main Docs page to your site menu. See https://isabelcastillo.com/docs/no-more-menu-item
* New - Added action hook in the single.php template file: organized_docs_single_after_nav
* New - Added action hook in the widget.php template file: organized_docs_before_widget. This lets you add custom content above the sidebar Table of Contents widget.
* Fix - Fixed PHP noticed for Undefined variable pub.
* Tweak - Deleted filter hook: od_docs_main_title. Instead, you can edit the Main Docs page title in settings.
* Tweak - Removed CSS ids: #isa-docs-main-title and ul#organized-docs-main

= 2.3.2 =
* New - Added support for author to Docs post type.
* Maintenance - Updated microdata with new schema.org guidelines for TechArticle and for Accelerated Mobile Pages project.

= 2.3.1 =
* Maintenance - Fixed a PHP warning for undeclared variable.
* Maintenance - Removed an unused function.

= 2.3 =
* New - List ALL posts in the Table of Contents sidebar widget even if not assigned to a child category. This is useful if you use the plugin for books. It will now simply list each post under the book title without using subheadings.
* New - Added filters to the microdata output.
* New - Added several actions to the single template and taxonomy template.
* New - Added a new action to allow insertion of more meta fields on Docs Categories.
* Maintenance - Updated language .pot file.
* Tweak - Cleanup unused variables.

= 2.2 =
* Fix - The taxonomy page for a sub-category was only showing a max of 10 posts. Now it shows all posts for that sub-category.
* Tweak - Updated structured data microdata properties.

= 2.1.1 =
* New - Option to show last updated date on single Docs articles.
* Tweak - Better handling of the Disable Comments on Docs option.
* Tweak - Updated the version in template files.

= 2.1 =
* New - All 4 template files have been updated. If you are using a custom template file for Docs in your theme, you must update the file for Docs to work properly. Please see the documentation, under What's New, for an easy link to grab the new template files.
* New - Option to sort main, top-level Doc items by alphanumerical order.
* New - The CSS has been rewritten to leave a more neutral style for the Docs nav menu and the Table of Contents widget. The entire layout has been made compatible with Twenty Fifteen theme, as well as remaining compatible with Twenty Fourteen, Twenty Thirteen, and Twenty Twelve. Please see the documentation, under What's New, for a list of all CSS changes.
* Optimization - The toggle option now uses pure JavaScript. There is no jQuery dependency.
* Optimization - Use an HTML entity for the print icon instead of Font Awesome. There is no more option to include Font Awesome.
* Fix - dynamic_css() was adding empty style tag to head in some cases.
* Tweak - Renamed the function sort_terms to sort_terms_custom.
* Tweak - Updated .pot translation file.

= 2.0.4 =
* New - option to toggle the list of individual Docs articles on the top-level category pages.
* New - option to toggle the list of individual Docs articles in the Table of Contents widget.
* Fix - remove several PHP warnings that occurred when viewing a single Doc while a category was not assigned to the Doc.
* Tweak - updated the URL for Setup Instructions.
* Maintenance - updated the Table of Contents widget to work with the WordPress 4.0 customizer.
* Maintenance - updated .pot translation file.

= 2.0.3 =
* Tweak: moved  prev/next nav links for single docs to a template tag for easier-to-customize template files.
* Tweak: put back missing comments into single template.
* Tweak: taller line-height on main docs page.
* Tweak: eliminated a PHP notice that was triggered in organized_docs_content_nav when sub-categories were not assigned.
* Tweak: eliminated 2 PHP notices that were triggered in organized_docs_post_nav.
* Tweak: updated `.pot` translation file.

= 2.0.2 =
* Fix: improved styling for mobile devices.
* New: option to disable the Docs Menu Link that get automatically added to your site. You can still add your own link in Appearance: Menus.
* Tweak: changed category label from just Category to Docs Category for better usability.
* Tweak: minified CSS for faster page load speed.

= 2.0.1 =
* NOTE: Please see changes for version 2.0.
* Fix: filter the content on single docs.

= 2.0 =
* NOTE: This update has many changes, including style changes, so, please read this entire changelog section.
* New: new template files eliminate the need to hijack sidebars. Easily make your custom docs templates by adding a folder named organized-docs to your theme. In that folder, you can add a custom single.php, taxonomy.php, archive.php, and sidebar.php. See our new templates directory to copy the originals.
* New: option to set custom sort order for single docs. You can sort alphabetically, by date, or by custom sort order number. You can also choose to sort in ascending or descending order.
* New: option to NOT list each single docs post on the top-level item page, nor in the Table of Contents sidebar. Enable this option if you want to list only the subheadings.
* New: option to change the main Docs slug. For example, you could change it to books.
* New: option to change the page title on the main Docs page.
* New: option to not load Font Awesome stylesheet if your theme, or other plugin, already loads it. Checking this will increase your page load speed. If left unchecked, it will only load Font Awesome on single Docs, in the footer, and only if you use the printer icon.
* New: Docs now include schema.org microdata for TechArticle on single Docs, and microdata for CollectionPage on Docs archives pages. There is an option to disable microdata.
* New: If you are NOT using Twenty Fourteen theme, and you did insert a call to twentyfourteen_post_nav() in order use single Docs navigation, please note that it is no longer necessary since we have a new template system. So, you can remove your call to twentyfourteen_post_nav().
* Fix: a subheading without a sort order number would not display in some instances.
* Fix: no longer overriding the _post_nav for the default WP themes.
* Deprecated: od_docs_main_title filter is deprecated and no longer needed since an option to change the main Docs title is now added. Also, this filter while in legacy-use returns only text, not HTML h1 element. If you are hooking this filter, please update it to return just the text, or remove it altogether in favor of the new option.
* Tweak: changed h2 page title element on Docs archive pages to h1. You may need to adjust size.
* Tweak: load styles in footer for increased page load speed. And load it only on Docs pages.
* Tweak: updated styles for Twenty Fourteen, Twenty Thirteen, and Twenty Twelve themes.
* Tweak: use singleton class.
* Tweak: no longer hiding the single docs title.
* Tweak: no longer necessary to manually drag the Table of Contents widget over to the Docs Widget Area.
* Tweak: Table of Contents widget will not give error if not on single docs page anymore. This makes it safe to add this widget anywhere, for example, when using your own custom templates with your own sidebar areas.
* Tweak: updated .pot language file.

= 1.2.2 =
* Fix: 2 files were not synced to svn: custom.php and the localization file.
* New: option to use title anchor text on Docs post nav links, instead of 'next' and 'previous'.
* New: option to disable comments on Docs.
* Maintenance: updated .pot file.

= 1.2.0 =
* New: option to hide custom sidebar IDs to avoid multiple Table of Contents widgets.
* New: option to hide printer icon and print link.
* New: Navigate through next and previous docs. If you are not using Twenty Fourteen theme, call twentyfourteen_post_nav() in your single.php to use this feature.
* Tweak: better styling and padding for compatibility with Twenty Fourteen theme. 
* Maintenance: updated .pot file.

= 1.1.10 =
* New: added .pot file for localization.
* Maintenance: reset option to update all docs posts with default sort order.
* Maintenance: removed warning from array_combine when docs category terms are missing.

= 1.1.9 =
* New: option to delete all Docs data upon uninstall.
* Fix: 1 line which caused posts to save order number as 99999 and ignore the custom number.

= 1.1.8 =
* Fix: Typo in function name stopped script from assigning default sort-order to existing posts.

= 1.1.7 =
* Fix: Docs would not display if custom sort-order was not set. Now, it is not necessary to set a custom sort oder. It remains optional.
* Maintenance: removed script to give subheadings a default order since no longer needed.

= 1.1.6.1 =
Bug fix: Custom sort-order for Categories was not saving.

= 1.1.6 =
* Fix: give default order to sub-headings. PLEASE UPDATE NOW.

= 1.1.5 =
* New: added sort order for Top-level Doc Items, and for Sub-headings, and for individual Doc articles.
* New: uninstall.php to remove docs, taxonomies, and custom term options upon uninstall.
* Fix: PHP error notices on admin Parent column if no category was assigned.
* Tweak: removed generator tag for less markup.
* Tweak: added links to 2 demos in the description.
* Maintenance: updated plugin URL in readme.
* Maintenance: tested and passed for WP 3.9 compatibility.
* Maintenance: Removed CSS styling for docs-template for better compatibility with Twenty Fourteen Theme. See https://isabelcastillo.com/docs/page-is-too-wide-and-not-centered-since-updating-to-1-1-5

= 1.1.4 =
* Maintenance: removed unused icons.

= 1.1.3 =
* Bug fix: Table of Contents Widget was showing up 3 times on Twenty Fourteen theme.
* New: added Print button to single docs.
* New: added link to Setup Instructions.
* Maintenance: added support for Twenty Fourteen Theme.
* Maintenance: updated the icon for Docs.
* Maintenance: removed PHP notices and errors.

= 1.1.2 =
* Bug fix: Main Docs page query was broken.
* Tested for WP 3.8 compatibility.

= 1.1 =
* Bug fix: slug for docs category taxonomy was broken.
* Tested for WP 3.7.1 compatibility.

= 1.0 =
* Initial release.

== Upgrade Notice ==

= 2.6.3 =
Fix - Some settings were not being saved.

= 2.6.1 =
Improved CSS styles for single Docs.

= 2.5.2 =
New feature for Docs that have only 1 post for their category.

= 2.5 =
New feature for Docs that have only 1 post for their category.

= 2.1 =
All 4 template files have been updated. If you update, you must also update your custom template files!

= 2.0.4 =
Removed several PHP warnings that occurred when viewing a single Doc while a category was not assigned to the Doc.

= 2.0.1 =
Fix: filter the content on single docs. NOTE Please see changes for version 2.0.

= 2.0 =
NOTE: This update has many changes, including style changes, so, please read changelog.

= 1.2.2 =
Fix: custom.php file was not synced to svn.

= 1.2.0 =
New: option to hide custom sidebar IDs to avoid multiple Table of Contents widgets.

= 1.1.9 =
Fix 1 line which caused posts to save order number as 99999 and ignore the custom number.

= 1.1.8 =
Fix: Typo in function name stopped script from assigning default sort-order to existing posts.

= 1.1.7 =
Fix: Docs would not display if sort-order was not set. Now, it is not necessary to set custom sort oder. 

= 1.1.6.1 =
Bug fix: Custom sort-order for Categories was not saving.

= 1.1.6 =
Fix: Give default order to sub-headings. New: set custom sort order.

= 1.1.5 =
New: set custom sort order for Top-level Doc Items, Sub-headings, and individual articles.

= 1.1.4 =
Bug fix: Table of Contents Widget was showing up 3 times on Twenty Fourteen theme.

