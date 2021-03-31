# Ghost Themes

This repository contains themes used for the [ZUAR, Inc](https://www.zuar.com) Ghost Themes.

## Setup
```
cd /path/to/theme
nvm use lts/dubnium
npm install
npm install -g gscan
```

## Build
```
npm run dev
```
The above command builds the theme and watches for changes.  To use the theme, run a local version of Ghost and
link the theme directory here.

```shell script
npm run zip
```
The `zip` command builds a zip file in `dist` that can be uploaded to the blog.

## Test


### Install Ghost locally
Start from the parent directory of this repository i.e. go to the root of this repo and do `cd ..`

```
mkdir ghost && cd ghost
nvm use lts/dubnium
npm install ghost-cli@latest -g
ghost install 2.37.0 --local
ghost stop
cd content/themes
ln -s ../../../ghostthemes/blog .
ln -s ../../../ghostthemes/helpcenter .
cd ../..
ghost start
```

The themes are now available unter 'Installed Themes' on the 'Design' tab of the admin interface.

