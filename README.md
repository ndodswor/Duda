    -------------MULTILANGUAGE script for DUDAONE [Raw Edition] README----------------
    This script allows site visitors to easily switch between displayed languages in 
    a site using flag icons representing countries commonly associated with that
    language. Page content and its translations must be created by the user.

    --------------------SUPPORTED LANGUAGES & THEIR SUFFIXES--------------------------
    English (en), Spanish (es), Catalan (ca), Czetch (cz), Chinese (cn), Korean (kr)
    German (de), Finnish (fi), French (fr) Swedish (se), Danish (dk), Dutch (no , nl), 
    Japanese (jp), and Hebrew (iw). If you wish to add more languages
    please consult the 'Customization' section.

    -----------------------------HOW THIS SCRIPT WORKS--------------------------------
    This script sends visitors to pages on the site with the same name and the 
    matching suffix (_en, _fr, etc) when the corresponding flag is clicked. If no 
    page exists with this suffix, the visitor will reach a 404 page. 

    These language flags will be displayed based on the suffix and order of 
    languages listed in the MLV.languages array.

    The script assumes that any page without a suffix was written in the language 
    set in the MLV.defaultLanguage variable.

    When a user visits the site again after leaving, a cookie (with default duration
    of one day) will direct them to the appropriate language home page.

    ----------------------------HOW TO USE THIS SCRIPT--------------------------------
    1. Create a DudaOne site with pages in the default language
    2. Duplicate each of the pages once for each language you wish to add. You should
        end up with, for example, three 'home' pages if you want your site to have 
        three languages. The page names can be whatever you wish (Incio, for example, 
        would be a good name for the home page in spanish)
    3. Rename the page URLs for your site's pages (in manage pages, click the gear 
        icon to the right of each page, then go to SEO & Settings and scroll down to 
        'page  URL') to match their equivalent page's URL, but followed by an 
        underscore and then the language suffix. For example: home becomes home_es, 
        gallery becomes gallery_es, et cetera.) You can find a list of supported 
        languages and their suffixes in the supported languages section above.
        Note: The default home page's URL is always 'home', and cannot be changed. 
    4. Paste this script into the site's header (go to menu, then site settings, then
        header HTML)
    5. Add an HTML element in your site's header or footer and add the code:
        <div class='multiLanguageRow'></div>
        to it. Where you place this code is where the multilanguage flags will show.
    6. Set the navigation to display 'all items'; Go to design -> navigation -> 
        customize (under desktop) -> settings and in the 'Number of visible desktop 
        navigation items' dropdown, select 'all items'.
    7. Set the tablet navigation to 'side' (the icon with a darker half of the page)
        and the mobile navigation to slide, list (the multiple boxes), or expanded 
        (the single box at the top right).
    9. Change the MLV.languages array to contain the suffixes of languages of the 
        pages you've added in the order you wish them to display
    10. Change the MLV.defaultLanguage variable to the suffix of the default language
        your site uses.
    
    ------------------------TROUBLESHOOTING / REQUIREMENTS----------------------------
    This script should be added to the header HTML of the site.
    
    For this script to work properly, it is necessary for all pages of the site to have
    equivalent pages built for each other language, following the schema: 
    pagename_languageID, so for example mypage_fr.
    
    Please note that whichever language is set to 'default language' below will default
    to page names without a language ID, so for example mypage.
    All home pages must also have the URL schema home_languageID, or at least load at 
    that URL.

    If this script is used on a site on which these pages do not exist, it can cause
    a 404 error or cause the editor not to load. To fix this, clear your browser cache
    and make the pages per the above specifications.

    Setting the navigation of the site to have 'All Items' displayed in the 'Number of 
    visible navigation items' is necessary to have pages display properly.

    Setting the tablet navigation to 'side' (the icon with a darker half of the page)
    and the mobile navigation to slide, list (the multiple boxes), or expanded 
    (the single box at the top right) is necessary for this to display correctly on
    those devices.

    This script may not work with some Duda templates; if this is the case, set the
    header to 'display as row' by going to design -> header -> display as row.

    It is possible to put the multiLanguageRow class in a div in the main body of the
    site, but due to the way animated navigation works in Duda, this may cause the 
    flags not to load, so I recommend turning it off. To turn off animated 
    navigation, go to design -> navigation -> customize (under desktop) -> settings 
    and set animated navigation to off.

    -------------------------------Customization-------------------------------------
    Add any languages you want in the 'MLV.languages' array (by suffix). They will 
    appear on the site in the order they appear in this array. The default language 
    will be the language that first loads for new visitors and the language assumed 
    for the home page.
    
    if you wish to add additional languages, it is necessary to modify the flag 
    datagram in the CSS styles at the end of this script, as well as modify the styles
    themselves to provide the appropriate offset. 

    --------------------------------END OF README------------------------------------*/
