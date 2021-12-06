# WEBPACK.__GB__
*introduccion*

- nos permite preparar codigo para llevarlo a produccion
- nacio en el 2012
- mapea el codigo tiene un punto de entrada y de salida 
- podemos implementar un modo de desarrollo local

*instalacion*
- `npm install webpack webpack-cli -D` webpack es el modulo 
- `npm install html-webpack-plugin -D` nos pormite ver en html
- `npm install webpack-dev-server -D` el servidor de webpack
webpack-cli es la consola -D en modo desarrollo
*configuracion*
- `webpack.config.js` 
```js
const HtmlWebpackPlugin = require("html-webpack-plugin")
module.export = {
  output :{
    filename:"app.bundle.js"
  },
  plugins:[
    new HtmlWebpackPlugin()
  ]
}
```
- `npx webpack` este es el modo produccion
- `npx webpack --mode development` modo desarrollo
