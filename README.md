# Rosie's BetterDiscord Themes
This is a git repository for BetterDiscord themes created by Discord user **Rosie#0530.** Feel free to use these how you see fit. Please remember to credit me if you use this elsewhere or share this with others (link to this git repository).

_**Last updated:**_ June 01, 2018

## Table of Contents
* [Basic Information](#basic-information)
    * [Contact Me](#contact-me)
    * [Latest Release Notes](#latest-release-notes)
    * [Planned Updates](#planned-updates)
* [Available CSS](#available-css)
    * [Theme Replacements](#theme-replacements)
    * [Component Changes](#component-changes)
* [How To Use](#how-to-use)
    * [Example Import](#example-import)
    * [Things to Note](#things-to-note)

## Basic Information
These themes are similar in design to the default Discord light and dark themes, with some adjustments to accommodate for a custom background and other personal enhancements.

### Contact Me
If you have any questions on how to use these themes, feel free to email me ([me@rosie.moe](me@rosie.moe)).

Suggestions, issues, and feedback should be given as bug reports here on Github for easier tracking. Please be as detailed as possible when submitting a bug report (screencaps are useful).

### Latest Release Notes
Made long-needed revisions to update the theming to accommodate for class changes made on Discord's end.

### Planned Updates
* Popout styles
* User profile styles
* Core background styles refactor
* More colored themes

## Available CSS

### Theme Replacements

#### Base theme (required)
**Description:** This is the base theme. Regardless of which other themes you use, you will need this to strip most of the default Discord theme styles to allow for customization.  
**URL:** `https://rawgit.com/rosieneko/betterdiscord-themes/master/css/base.css`

#### Default (Light) theme
**Description:** This replaces the default light theme. Make sure to choose the "light theme" in the Appearance tab for Discord user settings.  
**URL:** `https://rawgit.com/rosieneko/betterdiscord-themes/master/css/theme-main-light.css`

#### Default (Dark) theme
**Description:** This replaces the dark light theme. Make sure to choose the "dark theme" in the Appearance tab for Discord user settings.  
**URL:** `https://rawgit.com/rosieneko/betterdiscord-themes/master/css/theme-main-dark.css`

### Component Changes
#### 2-Column Server Lists

**Description:** This replaces the default 1-column list for the servers with a 2-column design. For those who like having all of their servers on the screen at once.  
**URL:** `https://rawgit.com/rosieneko/betterdiscord-themes/master/css/component-serverlist-2col.css`

## How To Use

To use these themes as they are, you can use the `@import` feature. For example, to import the base theme, you would use:


```css
@import 'https://rawgit.com/rosieneko/betterdiscord-themes/master/css/base.css';
```

If you prefer, you can copy the entire CSS code out of the file, and directly paste into your custom CSS editor. By doing so, you would not receive any additional changes in the future and would need to manually update each time changes are made. All compiled CSS URLs linked above under **[Available CSS](#available-css)**.

To include your own custom background, use the following CSS in the Custom CSS Editor for BetterDiscord after all the imports:

```css
div[class*=appMount-], div[class*=backdrop-] {
  background-image: url("HTTPS URL HERE") !important; 
}
```

`div[class*=appMount-]` and `div[class*=backdrop-]` are landscape-oriented spaces. `div[class*=appMount-]` targets the *main* container's background, while `div[class*=backdrop-]` targets the background that appears when you click on modal items (e.g., expanding the view of an image). You may use the same images or different images for those classes, depending on your preference.

Replace **URL HERE** with the image URL. Must be hosted on a server that uses HTTPS. My recommendation is to use [Imgur](https://imgur.com/).

**Please note:** None of themes will come with a custom background image, and they are designed with a custom background image in mind. You must supply this yourself.

### Example Import

If you wanted to use the modified light theme with a custom background and the 2-column server styles, you would put the following into your "Custom CSS" with BetterDiscord:

```css
@import 'https://rawgit.com/rosieneko/betterdiscord-themes/master/css/base.css';
@import 'https://rawgit.com/rosieneko/betterdiscord-themes/master/css/theme-main-light.css';
@import 'https://rawgit.com/rosieneko/betterdiscord-themes/master/css/component-serverlist-2col.css';

div[class*=appMount-], div[class*=backdrop-] {
  background-image: url("HTTPS URL HERE") !important; 
}
```

### Things to Note

These themes are based on appearance settings for font size and zoom level set at **100**. You will have some minor oddities if you change those settings.

When there is an update to the theme, it may not automatically appear for you if you are using the `@import` method. This is due to the cookies caching on your computer (and in Discord) for the CSS files.

You **may** need to clear the cookies for the rawgit site from your computer if you do not see new updates, or you may need to wait until Discord itself clears its cache of the CSS file. Usually it does not take more than a couple hours after the updates are pushed to the repository for it to refresh in Discord (may require restart of Discord, after Discord has cleared the cache).