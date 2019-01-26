# three.js-es6-webpack-starter

[![Renovate enabled](https://img.shields.io/badge/renovate-enabled-brightgreen.svg)](https://renovateapp.com/)
A minimal three.js ES6 starter project that uses webpack.

![A GIF file showing a preview of the starter project](https://github.com/jackdbd/threejs-es6-webpack-starter/blob/master/preview.gif "A scene with a spotlight, a directional light, a particle system, a custom material and several helpers.")

:warning: If you encounter a `validateschema` error when running `yarn dev`, try downgrading `webpack-cli` to `2.0.0`. It seems a bug that affects only [webpack-dev-server](https://stackoverflow.com/questions/50654952/webpack-dev-server-fails-to-run-with-error-of-validateschema). :warning:

### Features:

* ES6 support via [babel-loader](https://github.com/babel/babel-loader)
* CSS support via [style-loader](https://github.com/webpack-contrib/style-loader)
and [css-loader](https://github.com/webpack-contrib/css-loader)
* SASS support via [sass-loader](https://github.com/jtangelder/sass-loader)
* ES6 linting via [eslint](https://www.npmjs.com/package/eslint) and
[eslint-config-airbnb](https://www.npmjs.com/package/eslint-config-airbnb) or [prettier](https://github.com/prettier/prettier)
* SASS linting via [sass-lint](https://www.npmjs.com/package/sass-lint)
* Controls via [orbit-controls-es6](https://www.npmjs.com/package/orbit-controls-es6)
* GUI via [dat.GUI](https://github.com/dataarts/dat.gui)
* GLSL shaders support via [webpack-glsl-loader](https://www.npmjs.com/package/webpack-glsl-loader)
* Webpack configuration with:
  - [mini-css-extract-plugin](https://github.com/webpack-contrib/mini-css-extract-plugin)
  - [HtmlWebpackPlugin](https://github.com/jantimon/html-webpack-plugin)
  - [BundleAnalyzerPlugin](https://github.com/th0r/webpack-bundle-analyzer)
  - [CompressionPlugin](https://github.com/webpack-contrib/compression-webpack-plugin)
  - [CleanWebpackPlugin](https://github.com/johnagan/clean-webpack-plugin)

### Installation

```
git clone git@github.com:jackdbd/threejs-es6-webpack-starter.git
cd threejs-es6-webpack-starter

yarn install
```

### Usage

Generate all js/css bundles

```
yarn run build
```

Run `webpack-dev-server` (all bundles will be served from memory)

```
yarn run dev
```

If you have issues with old dependencies you can try to fix them by running:

```
yarn update:packages
```

Go to `localhost:8080` to see your project live!

Go to `localhost:8888` to analyze your webpack bundles with `BundleAnalyzerPlugin`


### Credits

The setup of this starter project was inspired by two snippets on Codepen: [this one](http://codepen.io/mo4_9/pen/VjqRQX) and [this one](https://codepen.io/iamphill/pen/jPYorE).

I understood how to work with lights and camera helpers thanks to
[this snippet](http://jsfiddle.net/f17Lz5ux/5131/) on JSFiddle.

The script which wipes all project's npm dependencies and reinstall them from scratch was found [here](https://medium.com/@_jh3y/how-to-update-all-npm-packages-in-your-project-at-once-17a8981860ea).

The code for `vertexShader.glsl` and `fragmentShader.glsl` is taken from
[this blog post](http://blog.cjgammon.com/threejs-custom-shader-material).

The star used in the particle system is the PNG preview of [this image](https://commons.wikimedia.org/wiki/File:Star_icon-72a7cf.svg) by Offnfopt
(Public domain or CC0, via Wikimedia Commons).
