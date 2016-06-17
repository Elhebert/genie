# Genie

Genie is a small packages.json that replace gulp/gruntfiles.

> See, all you gotta do is rub that lamp, and I'll say:
> "Mr. Aladdin, sir, what will your pleasure be?"
![genie](http://i.giphy.com/tpTOw6sljB2U.gif)

## Usage

To run one of the scripts, simply use the following syntax `npm run <scriptname>`

### Available scripts

__babel__: Compile es6 javacsript into es5 compatible javascript.
- _input_: `src` directory
- _output_: `dist/es5` directory

__linting__: Verify the linting of the javascript files (using jshint and jscs).
- _input_: All the available javascript files.
- _exclude_: `.node_modules` and `.bower_components`

__uglify__: Uglify and minify the javascript files
- _input_: Every `.js` files inside the `dist/es5`directory
- _output_: `dist/app.min.js`

__scss__: Compile the scss files into css.
- _input_: `src/styles/style.scss`.
- _output_: `dist/style.css` directory

__autoprefixer__: Parse css and add prefixes.
- _input_: `dist/style.css`
- _output_: `dist/style.css`

__serve__: synchronise your browser on file changes
- _files_: `dst/style.css`, `src/**/*.js`and `**/*.html`
- _address_: `localhost:3000`

__build:css__: Run the `scss` and `autoprefixer` scripts.

__build:js__: Run the `linting`, `babel` and `uglify` scripts.

__build:all__: Run `build:css` and `build:js`.

__watch:css__: Run `build:css` when a scss file is modified.

__watch:all__: run `serve` and `watch:css` in parallele.

## License
This script is published under the [MIT license](./LICENSE)