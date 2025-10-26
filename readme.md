# Fix pink youtube

> A browser add-on to make youtube red again

[Firefox](https://addons.mozilla.org/en-US/firefox/addon/fix-pink-youtube-progress/)
[Chrome](https://chromewebstore.google.com/detail/fix-pink-youtube)
## Reference

To make sure we use the right colors: we use a [07.05.2023 snapshot](https://web.archive.org/web/20230705011417/https://www.youtube.com/) from archive.org
there for reference we found a few different reds they used:

*07.05.2023 css variables*
```css
--yt-brand-youtube-red: #f00;
--yt-brand-medium-red: #c00;
--yt-brand-light-red: #ff4e45;
--yt-brand-medium-red-alpha-90: rgba(204, 0, 0, 0.9);
--yt-brand-medium-red-alpha-30: rgba(204, 0, 0, 0.3);
--yt-spec-brand-button-background: #c00;
--yt-spec-brand-button-background-hover: #990412;
--yt-spec-red-30: #ff8983;
--yt-spec-red-70: #990412;
--yt-spec-brand-link-text: #c00;
--yt-spec-error-indicator: #990412;
--yt-spec-static-brand-red: #f00;
--yt-spec-selected-nav-text: #c00
--yt-spec-static-overlay-background-brand: rgba(204, 0, 0, 0.9);
--yt-live-chat-count-color-error: hsl(10, 51%, 49%);
--yt-live-chat-error-message-color: hsl(10, 51%, 49%);
--yt-live-chat-mention-background-color: #ff5722;
--error-color: #dd2c00;
```

I may build a [little app](https://github.com/GREEB/color-changes) to better visualize color changes over time with a bunch of archive snapshots as soon as the API is up again.


## Features

- Changes the progress bar in the main player to red
- Changes the progress bar in thumbnails to red

![fix player image](media/fix-player.png)
![fix thumbnail image](media/fix-thumbnail.png)

This add-on will try to keep up with future changes that youtube makes to colors to keep it red

## Getting started

### 🛠 Build locally

1. Clone
1. Run `npm install` to install all required dependencies
1. Run `npm run build`

The build step will create the `distribution` folder, this folder will contain the generated extension.

### 🏃 Run the extension

Using [web-ext](https://extensionworkshop.com/documentation/develop/getting-started-with-web-ext/) is recommended for automatic reloading and running in a dedicated browser instance. Alternatively you can load the extension manually (see below).

1. Run `npm run watch` to watch for file changes and build continuously
1. Run `npm install --global web-ext` (only only for the first time)
1. In another terminal, run `web-ext run -t chromium`
1. Check that the extension is loaded by opening the extension options ([in Firefox](media/extension_options_firefox.png) or [in Chrome](media/extension_options_chrome.png)).

#### Manually

You can also [load the extension manually in Chrome](https://www.smashingmagazine.com/2017/04/browser-extension-edge-chrome-firefox-opera-brave-vivaldi/#google-chrome-opera-vivaldi) or [Firefox](https://www.smashingmagazine.com/2017/04/browser-extension-edge-chrome-firefox-opera-brave-vivaldi/#mozilla-firefox).

## Extensions created using this template

- [notlmn/copy-as-markdown](https://github.com/notlmn/copy-as-markdown) - Browser extension to copy hyperlinks, images, and selected text as Markdown.
