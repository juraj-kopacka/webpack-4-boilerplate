# Webpack 4.6 Boilerplate

This is a simple webpack (4.6) boilerplate. It's intention is to reduce time with new project basic webpack/stuff-compilation setup.

Main features:
* compiling js, css, html, ...
* webpack dev server with 2 modes - __simple__ or __proxy__ to existing nginx/apache server (php, ...)
* hot reloading browser after changes in js, css, php, html, ...


Modes:
* development mode: development server with hot reloading - refresh when js, styles, html, php, ... files change
* watch mode: compiles js and css after js and styles change
* production mode: builds production files


## Prerequisites

* [node.js](https://nodejs.org) - Node 9+
* [yarn](https://yarnpkg.com) - Yarn 1.5.1+ (yes, you can use `npm` instead, but the syntax in project is written for yarn)


## Instalation

```sh
yarn
```
All npm packages will unpack to `node_modules`.


## Modes

### Development mode - 2 cases incudeed
#### - simple dev server

```sh
yarn dev
```
Webpack dev server will launch, available at `http://localhost:8080`. All changes in `javascript`, `styles` and `html` files will be shown in browser immediately. Be aware - js and css files live only on dev server in this mode - js and css files in file structure will not change (for that you need production build or watch mode).

#### - dev server with proxy to existing nginx/apache server (beacuse of php, ...)

```sh
yarn dev:proxy
```
Webpack dev server will launch, it will open automatically in browser or it is available at `http://localhost:3000`. All changes in `javascript`, `styles`, `html` and `php` (or other types - depending on what you add to config) files will be shown in browser immediately. Be aware - js and css files live only on dev server in this mode - js and css files in file structure will not change (for that you need production build or watch mode).


### Watch mode

```sh
yarn watch
```
It is possible to launch watch mode - it means, that changes in `javascripte` and `styles` will launch compilation of js and css, but these files will be generated in **development form**. In this mode, the dev server is off, so you need to refresh the browser to see the changes.


### Production build

```sh
yarn build
```
Production `main.js` and `main.css` will be generaged (in **'/public/scripts'** a **'/public/styles'**).

## Fonts

Fonts need to be added to `/public/styles/fonts`.
New fonts need to be added to `/public/styles/fonts/fonts.scss` (fonts that are already there can serve as example).

## License
This is an open source project, you can do whatever you want with it (personally or commercialy) at your own risk; and I take no responsibility for whatever you do with it. 

* _put together by:_ [Juraj Kopacka](http://www.crioarts.sk/)
* _main inspiration and resources taken from:_ [bstaruk/starbase](https://github.com/bstaruk/starbase/) (major difference is, that I needed more sofisticated dev server with ability to hotreaload browser after changes in php files, ...)