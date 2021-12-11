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
const path = require('path')

module.exports = {
	/*el punto de entrada de nuestra app*/
	entry:'./src/index.js',
	/*el ouput de webpack*/
	output:{
		path:path.resolve(__dirname,'dist'),
		filename:'main.js',
	},
	/*extenciones vamos a trabajar en el proyect .js .ts .jsx*/
	resolve:{
		extensions:['.js']
	}
}
```
- podemos ir al package.json y crear un script 
```json
"build":"webpack --mode production"
/*no hace falta agregarle el webpack.config.js ya que al estar dentro
del json lo reconose por default*/
```
*code bash*
```bash
npx webpack `este es el modo produccion`
npx webpack --mode development `modo desarrollo`
npx webpack --mode production --config webpack.config.js `corre modo
production con la configuracion del archivo` 
```

