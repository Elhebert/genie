# Genie

Genie is a small packages.json that replace gulp/gruntfiles.

> See, all you gotta do is rub that lamp, and I'll say:
> "Mr. Aladdin, sir, what will your pleasure be?"

![genie](http://i.giphy.com/tpTOw6sljB2U.gif)

## Usage

To run one of the scripts, simply use the following syntax `npm run <scriptname>`

### Available scripts

#### `babel`: 
Compile es6 javacsript into es5 compatible javascript.
- _input_: `src` directory
- _output_: `dist/es5` directory

#### `linting`: 
Verify the linting of the javascript files (using jshint and jscs).
- _input_: All the available javascript files.
- _exclude_: `.node_modules` and `.bower_components`

#### `uglify`: 
Uglify and minify the javascript files
- _input_: Every `.js` files inside the `dist/es5`directory
- _output_: `dist/app.min.js`

#### `scss`: 
Compile the scss files into css.
- _input_: `src/styles/style.scss`.
- _output_: `dist/style.css` directory

#### `autoprefixer`: 
Parse css and add prefixes.
- _input_: `dist/style.css`
- _output_: `dist/style.css`

#### `serve`: 
synchronise your browser on file changes
- _files_: `dst/style.css`, `src/**/*.js`and `**/*.html`
- _address_: `localhost:3000`

#### `build:css`: 
Run the `scss` and `autoprefixer` scripts.

#### `build:js`: 
Run the `linting`, `babel` and `uglify` scripts.

#### `build:all`: 
Run `build:css` and `build:js`.

#### `watch:css`: 
Run `build:css` when a scss file is modified.

#### `watch:all`: 
run `serve` and `watch:css` in parallele.

## License
This script is published under the [MIT license](./LICENSE)
