# Preferente es realizar una clonación del repositorio
Es preferible una clonación del repositorio ya que algunas dependencias de desarrollo por sus actualizaciones tengan confictos, es mejor hacerlo con las que estar en el repositorio.
Pero si igual quieren hacerlo *paso a paso* tambien hay esa opción.

## Una instalación simple
si lo quiere quieres algo más simple y menos complicado de solo html, css y js.
**edteam** tiene blog donde te explica como hacerlo [enlace del blog](https://ed.team/blog/introduccion-webpack-4)

## Instrucciones
 1. Clonar el repositorio
 2. Instala los paquetes `npm install`
 3. Corre el proyecto con 3 opciones
    * `npm start` cargar en tiempo real
    * `npm run build` cargar en producción
    * `npm run dev` cargar en desarrollo
 4. Empezar el proyecto


# Instación paso a paso
## instalar webpack
  `npm install webpack webpack-cli -g`
  terminal
    `npm init`
  `npm install webpack webpack-cli -D`

 crear la carpeta src con el archivo index.js


## si quiere cambiar el lugar de origen de las carpetas

```javascript
"build": "webpack --mode production",
"dev": "webpack --mode development",
"build2": "webpack --mode production ./prueba/dev/main.js --output ./prueba/public/script.js",
"dev2": "webpack --mode development ./prueba/dev/main.js --output ./prueba/public/script.js"
```

## instalar babel
`npm i -D babel-loader babel-core babel-preset-env` || -D dependencias de desarrollo
crea una archivo .babelrc ( colocar presets)

  "build-babel": "webpack --mode production --module-bind js=babel-loader",
  "dev-babel": "webpack --mode development --module-bind js=babel-loader"

## desinstalar babel
`npm un -D babel-loader babel-core babel-preset-env`

## instalar babel 2
**(esto por si la version de webpack no soporta el babel actualizado)**
`npm i -D babel-core@6.26.3`
`npm i -D babel-loader@7.1.5`
`npm i -D babel-preset-env@1.7.0`

## instalar dependencias de html-plugin
`npm i -D html-webpack-plugin html-loader`

crear el archivo webpack.config.js || agregar los modules y plugins
*(guiate del **webpack.config.js** del respositorio)*

## dependencias en tiempo real
`npm i -D webpack-dev-server`
configurar en package.json || `"start": "webpack-dev-server --mode development --open",`

## el resto de las dependencias
**puede a ver problemas con las versiones de las dependencias, asi si una falla instalar la version del repositorio**
`npm i -D autoprefixer` ||
`clean-webpack-plugin` || correr una ejecucion en produccion puede limpiar la caperta de publicacion
`css-loader` || cargar las ojas de estilo
`file-loader` || si necesito un archivo tipo grafico
`image-webpack-loader` || cargar y optimar imagenes
`mini-css-extract-plugin` || sacar el codigo js los estilos css y llavarlo por una etiqueta link
`node-sass` ||
`postcss-loader` || autoprexiser
`resolve-url-loader` || louder de transformar de una manera correcta las url
`sass-loader` || transformar el codigo
`style-loader` || estilos en linea


`npm i -D autoprefixer clean-webpack-plugin css-loader file-loader image-webpack-loader mini-css-extract-plugin node-sass postcss-loader resolve-url-loader sass-loader style-loader`


## DEPENCIAS DE DESARROLLO PARA REACT VUE
`npm i -D babel-preset-react`
`npm i -D ts-loader`
`npm i -D typescript`
`npm i -D vue-loader`
`npm i -D vue-style-loader`
`npm i -D vue-template-compiler`

## DEPENDECIA VUE REACT
`npm install vue`
`npm install react react-dom`
