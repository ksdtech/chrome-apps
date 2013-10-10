chrome-apps
===========

A collection of Google Chrome apps we deploy to our Chromebooks.

ksd-bookmarks
-------------

Web shortcut/bookmark to http://kentfield.symbaloo.com

Development notes
-----------------

Here are some general instructions for privately publishing a Chrome app,
and then pre-installing it for your Google Apps domain.

1. Adjust Google Apps domain Settings > Chrome Management > User Setttings
    to allow for a private "For domain" collection on the Chrome Web Store 
    home page and, and to allow anyone to publish apps for the domain.
2. Prepare manifest.json and 128x128 icon in a folder ("static"). In the
    manifest, make sure you have a "short_name", 12 characters or less;
    the "name" can be up to 46 characters.
3. Also create a 640x400 screenshot and a 440x280 promotional tile image. 
    Place these in a separate folder ("store").
2. In Chrome, go to Settings > Extensions. Check the "Developer mode" box 
    to get access to unpacked extensions. Add the Chrome App with 
    "Load unpacked extension..." Test the app to make sure it works.
3. In "static" parent folder , zip -r bookmarks.zip static 
    to create bookmarks.zip file.
4. Log into Chrome with the account that will be publishing the app.
5. If you haven"t already, create a Google Site for all the apps that this
    user will be publishing and add a page for this app.
6. Navigate to the Web Store Developer Dashboard
    https://chrome.google.com/webstore/developer/dashboard
7. Click "Add an item".  You do not have to pay the $5.00 fee for publishing
    private apps for your domain.
8. Select and upload the .zip file created in step 3.
9. Fill in the metadata for the app: icon, screenshot, tile image, website,
    app page link on website, category ("Bookmarks"), language.
    Specify "Chrome Web Store users with a domain account" for the visibility.
    Click "Publish changes".
10. Update the Google Site with information about the app and provide a
    install link back to the Chrome Web Store.
11. Go back to Chrome Management and include the app in the pre-installed
    apps list.  You can find the app in the "Domain Apps" list.
    
Google App Engine
-----------------

Included in each app folder is an app.yaml file to serve up static files 
in case we start developing Python SDK-based apps as well.  It can be 
ignored for now.

