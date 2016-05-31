# excursion 1.0.0

## Install Packages

After cloning the project to your computer run the following command in your terminal to install all required node packages.

    sudo npm install

The first time you run gulp the build may take a little longer as it compiles and builds out the "public/css" and "public/js" folders and files.

## Running App
This build system can be run in two modes: development and production.  Use development when you are developing your app.  In this mode your JS will not be minified, React will include all its warnings and your CSS will contain sourcemaps to the original SCSS files.  When you are ready to deploy you can start the app in production mode which will turn off React warnings, uglify your JS, and turn off sourcemaps for both JS and CSS.

    npm start  (starts app in development mode)  
    npm run production (starts app in production mode)

## Important

When using "npm start" you are running react in 'development mode'.  "npm run production" runs react in 'production mode' removing many of React 15.0+ warnings.  See this link for more info [http://facebook.github.io/react/downloads.html](http://facebook.github.io/react/downloads.html).


## Features

- ES6+ with Babel.  Use all the new niffty ES6+ features and transpile down to ES5.
- Browserify: JSX transforms, ES6 modules.
- React Ready!
- Uglify: minification.
- BrowserSync.
- Sass / flexbox ready (IE10+), layout for everygreen browsers.

## How to use

Precompiled JS and SCSS files are in the src folder and compile to public.  All other files including HTML, image etc. are in public.  BrowserSync runs from public and serves as the "Dist" folder for client-side apps.


## To Do
- more testing

## How to remove React
If you would like to remove React from the build just follow the steps below.

1. In terminal remove react packages.

		npm uninstall react react-dom react-router --save

2. In gulpfile.js

	Remove lines:

		var react = require('react');

3. In folder: 'src/' remove components folder and 'routes.js'.
4. In file 'src/js/index.js' remove all code.  Add your new code to this file.
