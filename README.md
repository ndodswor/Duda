    -------------MULTILANGUAGE script for DUDAONE [Raw Edition] README----------------
    This script allows site visitors to easily switch between displayed languages in 
    a site using flag icons corresponding to the selected language's country.

    ----------------------------HOW TO USE THIS SCRIPT--------------------------------
    1. Create a DudaOne site with pages in the default language without an extension
    2. Duplicate each of the pages once for each language you wish to add. You should
    end up with, for example, three 'home' pages if you want your site to have three
    languages. The page names can be whatever you wish (Incio, for example, would be
    a good name for the home page in spanish)
    3. Re-name the page URLs for these pages (in manage pages, click the gear icon to
    the right of each page, then go to SEO & Settings and scroll down to 'page URL') 
    to match their parent page's URL, but followed by an underscore and then the
    language extension. For example: about becomes about_es, gallery becomes 
    gallery_es, et cetera. For the home pages, the page URL should just be the suffix
    (so the home page for spanish would be _es, for french would be _fr, etc.)
    4. Paste this script into the site's header (go to menu, then site settings, then
    header HTML)
    5. Add the placement div <div class='multiLanguageRow'> into an HTML element on 
    the site
    6. Set the navigation to display 'all items'; Go to design -> navigation -> 
    customize (under desktop) -> settings and in the 'Number of visible desktop 
    navigation items' dropdown, select 'all items'.
    7. Set the tablet navigation to 'side' (the icon with a darker half of the page)
    and the mobile navigation to slide, list (the multiple boxes), or expanded 
    (the single box at the top right).
    
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

    -------------------------------Customization-------------------------------------
    Add any MLV.languages you want in the 'languages' array (by suffix). They will 
    appear on the site in the order they appear in this array. The default language 
    will be the language that first loads for new visitors and the language assumed 
    for pages without a language ID suffix.
    
    if you wish to add additional languages, it is necessary to modify the flag 
    datagram in the CSS styles at the end of this script, as well as modify the styles
    themselves to provide the appropriate offset. 

    --------------------------------END OF README------------------------------------*/
