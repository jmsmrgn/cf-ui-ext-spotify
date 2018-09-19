Spotify search Contentful UI Extension
======================================

Auto-complete Spotify search as [Contentful UI Extension](https://www.contentful.com/developers/docs/concepts/uiextensions/).

![figure](https://raw.githubusercontent.com/tuunanen/cf-ui-ext-spotify/master/assets/demo.gif "Spotify search Contentful UI Extension demo")

## Features

* Auto-complete Spotify (track) search
* Preview for selected Spotify entry in a pop-up window
* Support for single Spotify entry per Contentful field

### Installation

```sh
yarn
```

### Configure

Rename `.env.example` to `.env` and add your Contentful space ID and Spotify access token. [Learn how to obtain a token](https://developer.spotify.com/documentation/general/guides/authorization-guide/).

Load environment variables

```sh
source .env
```

### Build

```sh
yarn run build:dev
yarn run build:production
```

Files processed by the build task will be located under `dist` directory.

### Create

```sh
yarn run create-extension
```

Create task will register the extension in your space on Contentful.

### Update

```sh
yarn run update-extension
```

Update task will upload the extension to your space on Contentful.

## How to add Spotify search field to content type

1. Select any content type under the *Content Model* content type list. [See screenshot](https://raw.githubusercontent.com/tuunanen/cf-ui-ext-spotify/master/assets/instructions-step-1.png).
2. Click *Add field* button. [See screenshot](https://raw.githubusercontent.com/tuunanen/cf-ui-ext-spotify/master/assets/instructions-step-2.png).
3. Select *JSON Object* as the field type. [See screenshot](https://raw.githubusercontent.com/tuunanen/cf-ui-ext-spotify/master/assets/instructions-step-3.png).
4. Fill in *Name* and *Field ID* and click *Create and configure*. [See screenshot](https://raw.githubusercontent.com/tuunanen/cf-ui-ext-spotify/master/assets/instructions-step-4.png).
5. Select *Appearance* tab. [See screenshot](https://raw.githubusercontent.com/tuunanen/cf-ui-ext-spotify/master/assets/instructions-step-5-7.png).
6. Select *Spotify search*
7. Hit *Save*

### Development

```sh
yarn run dev
```

Development task starts a development server at [http://localhost:8000](http://localhost:8000), and tells the Contentful App to load the extension from there instead of loading it from the API.

If you now open an entry that uses the extension in your browser it will use the code from your local machine. Please note that **you need to enable insecure content** since the Contentful App is served through HTTPS but your extension is not. Learn how to enable insecure content in [Firefox](https://support.mozilla.org/en-US/kb/mixed-content-blocking-firefox) and [Chrome](https://support.google.com/chrome/answer/1342714).

### Changelog

Please see [changelog](https://github.com/tuunanen/cf-ui-ext-spotify/blob/master/CHANGELOG.md).

### License

Copyright &copy; tuunanen

Licensed under the [MIT license](https://github.com/tuunanen/cf-ui-ext-spotify/blob/master/LICENSE).
