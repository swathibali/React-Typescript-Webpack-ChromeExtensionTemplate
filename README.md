# React Chrome Extension BoilerPlate

## Gettimg Started

1. `npm i` to install dependencies
2. `npm start` to running the fast development mode webpack build process that bundle files into the `dist` folder
3. `npm i --save-dev <package_name>` to install new packages

## Loading the chrome extension

1. Ppen Chrome an navigate to `chrome://extensions/`
2. Toggle on `Developer mode` in the top right corner
3. Click `Load unpacked`
4. Selec the entire `dist` folder

# Important Initial steps

1. `git init` to start a new git repo for tracking your changes, do an initial base commit with all the default files
2. Update `package.json` important fields include `author`, `version`, `name`, `description`,
3. Update `manifest.json`, important fields include `version`, `name`, `version` and `description`
4. Update `webpack.common.js`, the title in the `getHtmlPlugin` function should be your extenson name

# Production Build

1. `npm run build` to generate a minimized production build in the `dist` folder
2. ZIP teh entore dist folder (e.g. `dist.zip`)
3. Publisgh the ZIP file on the chrome Web Store Developer Dashboard!

## Important default BOilerplate notes

- Folders get flattened, sttaic references to images from HTML do not need to be relative(i.e. `icon.png` instead of `../static/icon.png`)
- Importing local ts/tsx/css files should be relative, since webpack will build a dependency grapgh using these paths
- Updae the manifest file as per usual for chrome related permissions, references to files in here should also be falttened and not to be relative
