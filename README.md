Multilanguage script
This script allows site visitors to easily switch between displayed languages in a site using a dropdown by selecting the desired language's name. Page content and its translations must be created by the user.

How this script works

This script creates a dropdown element from which visitors can select a language. Doing so sends them to a page with the same name and a suffix matching the selected language (_eng, _fra, etc.)

The names in this dropdown will be displayed based on the suffix and order of languages listed in the MLV.languages array.

The script assumes that the home page was written in the language set in the MLV.defaultLanguage variable.

When a user visits the site again after leaving, a cookie (with default duration of one day) will direct them to the appropriate language home page.

Please note that this script does not work with eCommerce or Blogs.

How to use this script

Create a DudaOne site with pages in the default language
Duplicate each of the pages once for each language you wish to add. You should end up with, for example, three 'home' pages if you want your site to have three languages. The page names can be whatever you wish (Incio, for example, would be a good name for the home page in spanish)
Rename the page URLs for all of your site's pages (in manage pages, click the gear icon to the right of each page, then go to SEO & Settings and scroll down to 'page URL') to match their equivalent page's URL, but followed by an underscore and then the language suffix. For example: the home page becomes home_spa, gallery_eng becomes gallery_spa, et cetera.) The visible names of the pages can be whatever you like; only the URLs need to be customized in this way.You can find a list of supported languages and their suffixes in the Supported Languages section above. Note: The default home page's URL is always 'home', and cannot be changed.
Paste this script into the site's header (go to menu, then site settings, thenheader HTML)
Add an HTML element in your site's header and footer and add the code:
to it. Where you place this code is where the multilanguage dropdown will show. Please note that this will not show up in the header of the mobile site due to limitations of the platform.
Set the navigation to display 'all items'; Go to design -> navigation -> customize (under desktop) -> settings and in the 'Number of visible desktop navigation items' dropdown, select 'all items'.
Set the tablet navigation to 'side' (the icon with a darker half of the page)and the mobile navigation to 'slide', 'list' (the multiple boxes), or 'expanded' (the single box at the top right). Please refer to the below image if this is unclear; navigation styles with red borders are not supported. Change the MLV.languages array to contain the suffixes of languages of the pages you've added in the order you wish them to display.
supported-templates.png
Change the MLV.defaultLanguage variable to the suffix of the default language your site uses.
Troubleshooting / requirements

This script should be added to the header HTML of the site.

For this script to work properly, it is necessary for all pages of the site to have equivalent pages built for each other language, following the schema: pagename_languageID, so for example mypage_fr.

Please note that whichever language is set to 'default language' below will default to page names without a language ID, so for example mypage. All home pages must also have the URL schema home_languageID, or at least load at that URL.

If this script is used on a site on which these pages do not exist, it can cause a 404 error or cause the editor not to load. To fix this, clear your browser cache and make the pages per the above specifications.

Setting the navigation of the site to have 'All Items' displayed in the 'Number of visible navigation items' is necessary to have pages display properly.

Setting the tablet navigation to 'side' (the icon with a darker half of the page) and the mobile navigation to slide, list (the multiple boxes), or expanded (the single box at the top right) is necessary for this to display correctly on those devices.

This script may not work with some Duda templates; if this is the case, set the header to 'display as row' by going to design -> header -> display as row.

It is possible to put the multiLanguageRow class in a div in the main body of the site, but due to the way animated navigation works in Duda, this may cause the dropdown not to load, so I recommend turning it off. To turn off animated navigation, go to design -> navigation -> customize (under desktop) -> settings and set animated navigation to off.

Please note that this script does not work with eCommerce or Blogs.

Supported languages & their suffixes

By default, this script supports the 20 most common languages used on the internet, as defined by wikipedia, using the ISO 639-2/T format for three-letter suffixes. At the time of this writing, these are: Arabic (ara), Chinese (zho), Czetch (cze), German (deu), English (eng), French (fra), Greek (ell), Indonesian (ind), Japanese (jpn), Korean (kor), Persian (fas), Polish (pol), Vietnamese (vie), Portuguese (por), Spanish (spa), Swedish (swe), and Turkish (tur). If you wish to add more languages please consult the Customization section.

Customization

Add any languages you want in the 'MLV.languages' array (by suffix). They will appear on the site in the order they appear in this array. The default language will be the language that first loads for new visitors and the language assumed for the home page.

if you wish to add additional languages, just add the language to the MLV.languageName associative array using the language suffix as a key; please refer to the existing languages in the array for examples. You can find a list of official ISO suffixes and language names in the Wikipedia article List of ISO 639-1 codes.
