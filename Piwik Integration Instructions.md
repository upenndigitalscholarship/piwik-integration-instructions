# Piwik Integration Instructions

Sasha Renninger

For each site that requires integration:
1. Go to [http://upenndigitalscholarship.org/piwik/](http://upenndigitalscholarship.org/piwik/)
    * Log in
    * Click on "All Websites" in the upper right
    * Click on "Add a new website" in the center right
    * Edit the following fields:
        * __Name__: Use the name of the site on the home page
        * __URLs__: Copy and paste the url from the home page
        3. __Time zone__: Change to "New York"
    * Save
2. After you save, the new tracked website should appear in the list at the bottom of the page (you can also go to a list of all tracked websites by clicking "All Websites" in the upper right)
    * Click "View Tracking Code" for the website tracker you just created
    * Scroll down to the "Javascript Tracking Code". Copy the entire thing, including comments (you will be using this several times, so please refer back to it every time the instructions say to "paste the Piwik Javascript Tracking Code" - it should look like this):

``` 
<!-- Piwik -->
    <script type="text/javascript">
      var _paq = _paq || [];
      // tracker methods like "setCustomDimension" should be called before "trackPageView"
      _paq.push(['trackPageView']);
      _paq.push(['enableLinkTracking']);
      (function() {
        var u="//upenndigitalscholarship.org/piwik/";
        _paq.push(['setTrackerUrl', u+'piwik.php']);
        _paq.push(['setSiteId', '10']);
        var d=document, g=d.createElement('script'), s=d.getElementsByTagName('script')[0];
        g.type='text/javascript'; g.async=true; g.defer=true; g.src=u+'piwik.js'; s.parentNode.insertBefore(g,s);
      })();
    </script>
<!-- End Piwik Code -->
```
3. **For Omeka sites:**
    * Go to [https://portal.reclaimhosting.com/clientarea.php](https://portal.reclaimhosting.com/clientarea.php)
        * Log in with your credentials
        * Click on "cPanel" on the top of the screen
        * On the next screen, click on "File Manager" at the top of the page
        * You should now see a file list. Double click on `public_html` in the file list in the middle of the page
        * Navigate to the folder containing all the Omeka code
        * Double click on `themes`
        * **For every folder in `themes`:**
            * Double click on the folder, then on "common"
            * Right click `header.php` and then “Code Edit”
            * Find the closing `</head>` tag
            * Right **above** the `</head>` tag, paste the Piwik Javascript Tracking Code for this site
            * **DO NOT FORGET TO CLICK "Save Changes" IN THE UPPER RIGHT**
4. **For WordPress sites:**
    * Go to [https://portal.reclaimhosting.com/clientarea.php](https://portal.reclaimhosting.com/clientarea.php)
        * Log in with your credentials
        * Click on "cPanel" on the top of the screen
        * On the next screen, click on "File Manager" at the top of the page
        * You should now see a file list. Double click on `public_html` in the file list in the middle of the page
        * Navigate to the folder containing all the WordPress code, then `wp-content`, and then `themes`
        * **For every folder in `themes`:**
            * Double click on the folder
            * Right click `header.php` and then “Code Edit”
            * Find the closing `</head>` tag
            * Right **above** the `</head>` tag, paste the Piwik Javascript Tracking Code for this site
            * **DO NOT FORGET TO CLICK "Save Changes" IN THE UPPER RIGHT**
5. **For Esri StoryMap sites:**
    * Go to [https://portal.reclaimhosting.com/clientarea.php](https://portal.reclaimhosting.com/clientarea.php)
        * Log in with your credentials
        * Click on "cPanel" on the top of the screen
        * On the next screen, click on "File Manager" at the top of the page
        * You should now see a file list. Double click on `public_html` in the file list in the middle of the page
        * Navigate to the folder containing all the StoryMap code
        * Right click `index.html` and then “Code Edit”
        * Find the closing `</head>`tag
        * Right **above** the `</head>`tag, paste the Piwik Javascript Tracking Code for this site
        * **DO NOT FORGET TO CLICK "Save Changes" IN THE UPPER RIGHT**
6. **For Weebly sites:**
    * Go to [https://www.weebly.com/](https://www.weebly.com/)
        * Log in
        * Click "Edit Site" in the upper right
        * Click on "Settings" at the top, and then “SEO” in the left menu
        * Paste the Piwik Javascript Tracking Code for this site in the "Footer Code" box
        * **DO NOT FORGET TO CLICK "Save" IN THE UPPER RIGHT**
7. **For Jekyll sites:**
    * Go to Jekyll repo on Github
        * Click on  the `_includes` directory
        * Open `head.html` to edit
        * Find the closing `</head>` tag
        * Right above the `</head>` tag, paste the Piwik Javascript Tracking Code for this site       
8. After you have finished pasting in the tracking code, browse around to a couple of pages on the website and then go back to the Piwik dashboard to make sure it is recording your activity (To get to the dashboard for a site, click on "All websites" and then the name of the website you are working on)
9. If you can see your activity, you are done!!!!!!!!!! If you can’t, time to troubleshoot!

