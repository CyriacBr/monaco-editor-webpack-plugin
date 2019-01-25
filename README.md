Work exactly like the original plugin, except that you can pass in the options an array of your custom languages for working with `monaco-typescript-embeddable`.

* `webpack.config.js`:
```js
const MonacoWebpackPlugin = require('monaco-editor-webpack-plugin-embeddable');

module.exports = {
  entry: './index.js',
  output: {
    path: path.resolve(__dirname, 'dist'),
    filename: 'app.js'
  },
  module: {
    rules: [{
      test: /\.css$/,
      use: ['style-loader', 'css-loader']
    }]
  },
  plugins: [
    new MonacoWebpackPlugin({
      embeddableLangs: ['myCustomLang']
    })
  ]
};
```
