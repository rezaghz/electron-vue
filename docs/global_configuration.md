# Global Configuration

electron-vue uses the [webpack/webpack](https://github.com/webpack/webpack) module loader system for pre-processing, bundling, and building your app. The default settings are rather common and should meet most of your needs and a `config.js` is provided in the root directory for quick adjustments. Further customizations can be made by directly adjusting `webpack.config.js`.

#### ``config.js``
```js
{
  // Enable electron's devtron devtools extension in development
  devtron: true,

  // webpack-dev-server port
  port: 9080,

  // Enable vue-devtools in development
  vueDevTools: true,
  
  // electron-packager options
  // See `Building you app` for more info
  building: {
    'app-version': pkg.version,
    arch: 'x64',
    asar: true,
    dir: path.join(__dirname, 'app'),
    icon: path.join(__dirname, 'app/icons/icon'),
    ignore: /node_modules|src|main.html|icons/,
    name: pkg.name,
    out: path.join(__dirname, 'builds'),
    overwrite: true,
    platform: 'all'
  }
}
```
**NOTE**

At the moment, the configuration options are rather sparse. More will continually be added as needed.