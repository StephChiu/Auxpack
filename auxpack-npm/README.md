# auxpack
auxpack is the configurable Webpack plugin that monitors statistics from your production builds. Our interactive interface allows developers to better understand bundle composition to get a better grasp on optimization strategies.

## Installation

Install via `npm i -D auxpack`

## Setup

```javascript
// webpack.config.js

const Auxpack = require('auxpack'); // import auxpack

modules.exports = [
// other configurations
  ... 
  plugins: [
    ...
    new Auxpack(  // add Auxpack into plugins
      {
        PORT: 1111, // configurable PORT
        targetFile: 'aux-stats', // configurable output filename
        logMe: true, // configure with true to console.log the current build's aux-stats
      }
    ),
  ]
  ...
]

```

## Usage

By installing the plugin into your Webpack configuration, you can run 
`webpack`
within your scripts as you would in production bundling, and our plugin will launch on port 1111. (or your chosen port in webpack.config.js)

Please note that collecting information on your first auxpack build may take a moment; this occurs due to our plugin collecting data.

## Contributing

To contribute to `auxpack`, please fork this repository, clone it to your machine, then install dependencies with `npm install`. If you're interested in joining the auxpack team as a contributor, feel free to message one of us directly!

## Authors

* Connie Lai (https://github.com/connielion)
* Nobuhide Ajito (https://github.com/najito)
* Stephanie Chiu (https://github.com/stephkchiu)
* Travis Clark (https://github.com/tm-clark)

# webpack-monitor

Many thanks to Webpack Monitor for passing the torch.
https://github.com/webpackmonitor/webpackmonitor

## License

This project is licensed under the MIT license - see the LICENSE.md file for details