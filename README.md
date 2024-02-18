# firefox-css

> Fork of [firefox-csshacks](https://github.com/MrOtherGuy/firefox-csshacks)

Contains customizations for Firefox's userChrome.css and userContent.css files. 
These files allow for the customization of the Firefox UI and webpages.

## Setup 

## Set the pref to load stylesheets
Go to `about:config` and set the pref `toolkit.legacyUserProfileCustomizations.stylesheets` to `true`
After you set this pref, Firefox will try to load `userChrome.css` and `userContent.css`.

### Find the profile folder
First, find your profile folder. While Firefox is running, go to `about:support` and find a `Profile folder` row near the top - there should also be a button labeled "Open folder" next to it. Clicking that button should open the folder in your file manager.
> NOTE: On some Firefox versions clicking that button may open the **profiles** folder which houses *all* your profiles. In that case, navigate into the specific folder you wish to modify. `about:support` should still show the correct folder name so refer to that if you need to figure out the what folder you need to open. 
The real profile folder should have files like `prefs.js` and `places.sqlite` If you see those two files in the folder, then great! You found the profile folder! Now lets actually create those stylesheet files.

### Set up files using git
<details>
<summary>Preferred way to do things, since it makes updates easier and makes organizing multiple styles easier.</summary>

Assumes that you have a git client installed, and that you do not already have a chrome folder in your profile. 

1. Open a command prompt / console / terminal and `cd` into the profile folder
2. Clone this repository into the profile folder
    * `git clone https://github.com/rabume/firefox-css.git chrome` on command-line
    * This should create a new folder "chrome" into your profile folder with the contents of this repository
    * (**NOTE**: if you already have "chrome" folder, then rename it before cloning. After clone is complete, just copy the *contents* of the old folder into the new chrome folder)
3. You should now have a `userChrome.css` file in `<profileFolder>/chrome/userChrome.css` and `userContent.css` in `<profileFolder>/chrome/userContent.css`

Now you can alyways update the files by running `git pull` in the `chrome` folder. This will fetch the latest changes from the repository and apply them to your local files.

</details>
