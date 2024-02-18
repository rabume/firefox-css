# firefox-css

> Fork of [firefox-csshacks](https://github.com/MrOtherGuy/firefox-csshacks)

Contains customizations for Firefox's userChrome.css and userContent.css files. 
These files allow for the customization of the Firefox UI and webpages.

## 🔧 Setup 
1. Enable loading of custom stylesheets
    * Go to `about:config` and set the pref `toolkit.legacyUserProfileCustomizations.stylesheets` to `true`
2. Find your profile folder
    * While Firefox is running, go to `about:support` and find a `Profile folder` row near the top - there should also be a button labeled "Open folder" next to it. Clicking that button should open the folder in your file manager.
3. Open a command prompt / console / terminal and `cd` into the profile folder
2. Clone this repository into the profile folder
    * `git clone https://github.com/rabume/firefox-css.git chrome` on command-line
    * This should create a new folder "chrome" into your profile folder with the contents of this repository
    * (**NOTE**: if you already have "chrome" folder, then rename it before cloning. After clone is complete, just copy the *contents* of the old folder into the new chrome folder)
3. You should now have a `userChrome.css` file in `<profileFolder>/chrome/userChrome.css` and `userContent.css` in `<profileFolder>/chrome/userContent.css`

Now you can alyways update the files by running `git pull` in the `chrome` folder. This will fetch the latest changes from the repository and apply them to your local files.
