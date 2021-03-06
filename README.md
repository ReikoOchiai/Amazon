# Amazon

Amazon Clone website

"Create Folder Structure"

1. Create root folder as Amazon
2. add frontend and backend folder
3. create src folder in frontend
4. create index.html with heading Amazon in src
5. run npm init in frontend folder
6. npm install live-server
7. add start command as live-server src --verbose
8. run npm start

"Design website"

1. create style.css
2. link style.css to index.html
3. create div.grid-container
4. create header, main and footer
5. style html, body
6. style grid-container, header, main and footer

"Create static home screen"

1. create ul.products
2. create li
3. create div.product
4. add .product-image, .product-name, .product-brand, .product-price
5. style ul.products and internal divs
6. duplicate 2 times to show 3 products

"Render Dynamic Home Screen"

1. create data.js
2. export an array of 6 products
3. create screen/HomeScreen.js
4. export HomeScreen as an object with render() method
5. implement render()
6. import data.js
7. return products mapped to lis inside and ul
8. create app.js
9. link it to index.html as module
10. set main id to main_container
11. create router() function
12. set main_container innerHTML to HomeScreen.render()
13. set load event of window to router() function

"Build URL Router"

1. create routes as route:screen object for home screen
2. create utils.js
3. export parseRequestURL()
4. set url as hash address split by slash
5. return resource, id and verb of url
6. update router()
7. set request as parseRequestURL()
8. build parsedUrl and compare with routes
9. if route exists render it, else render Error 404
10. create screens/Error404.js and render error message

"Create Node.JS Server"

1. run npm init in root of Amazon folder
2. npm install express
3. create server.js
4. add start command as node backend/server.js
5. require express
6. move data.js from frontend to backend
7. create route for /api/products
8. return products in data.js
9. run npm start

"Load Products From Backend"

1. edit HomeScreen.js
2. make render async
3. fetch products from '/api/products' in render()
4. make router() async and call await HomeScreen.render()

"Add Webpack"

1. cd frontend
2. npm install -D webpack webpack-cli webpack-dev-server
3. npm uninstall live-server
4. "start": "webpack-dev-server --mode development --watch-content-base --open"
5. move index.html, style.css and images to frontend folder
6. rename app.js to index.js
7. update index.html
8. add <script src='main.js'></script> before </body>
9. npm start
10. npm install axios
11. change fetch to axios in HomeScreen

"Install Babel for ES6 Syntax"

1. npm intall -D babel core, cli, node, preset-ev
2. Create .babelrc and set presets to @babel/preset-env
3. npm intall -D nodemon
4. set start: nodemon --watch backend --exec babel-node backend/ server.js
5. convert require to import in server.js
6. npm start

"Enable Code Linting"

1. npm intall -D eslint
2. install VSCode eslint extension
3. create .eslintrc and set module.exports for env to node
4. set VSCode setting for editor.codeActionsOnSace source.fixAll.eslint to true
5. check result for linting error
6. npm intall eslint-config-airbnb-base and eslint-plugin-import
7. set extends to airbnb-base
8. set parserOptions to ecmaVersion 11 and sourceType to module
9. set rules for no-console to 0 to ignore linting error

"Create Rating Component"

1. create components/Rating.js
2. create div.rating
3. link to fontawesome.css in index.html
4. define Rating object with render()
5. if !props.value return empty div
6. else use fa fa-star, fa-star-half-o and fa-star-o
7. last span for props.text || ''
8. style div.rating, span and last span
9. edit HomeScreen
10. add div.product-rating and use Rating component
