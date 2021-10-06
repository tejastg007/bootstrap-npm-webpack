
# Bootstrap installation with NPM



## Documentation



  
## initialize the directory
### npm init -y

## install webpack and webpack cli
### npm i -D webpack webpack-cli

## install bootstrap, popper js and jquery
### npm i  npm i bootstrap@4.6.0 @popperjs/core jquery
this will intall the core dependencies of the project.

## install dev dependencies
### npm i -D  npm install auto-prefixer node-sass sass-loader style-loader css-loader postcss-loader export-loader postcss
postcss, postcss-loader = process the postcss with loader
node-sass, sass-loader = loader for sass/scss files
style-loader = inject css into DOM
css-loader = The css-loader interprets @import and url() like import/require() and will resolve them.
export-loader = if importing bootstrap plugins then export-loader is required

## add script in package.json file
### "build":"webpack"
### "build:w":"webpack -w"

## create webpack config file with correct configuration
add entry point and outfile destination folder if any else it will take default source and destination files.
check the webpack.config.js file in the current directory for more understanding.


## postcss plugins 
you can add the postcss plugins in the webpack configuration.

alternatively, you can also define a postcss.config.js file

## including bootstrap
create scss folder in src directory and create app.scss file
import the all bootstrap scss files by-
#### @import bootstrap/scss/bootstrap"
then include this app.scss file in the entry point file i.e. app.js
#### import "./scss/app.scss"


## compile the assets now
### npm run build
this will build the bootstrap files from node-modules and create bundles in the destination folder

## to use the jquery in the prject, add the following lines in the app.js entry file
#### var $ = require("jquery");
#### window.jQuery = $;
#### window.$ = $;

## adding bundle file in the html 
now, the bundle is created by the webpack. just add that in the script tag and you are ready to go.