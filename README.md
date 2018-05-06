# amplify

Build AMP Pages quickly. Minify/compress files. AMP validation from the command line. [Learn more about AMP](https://www.ampproject.org/learn/overview/).

## Getting Started

```sh
$ git clone https://github.com/nickFalcone/amplify.git
$ cd amplify
$ npm install
$ gulp
```

## What amplify does
amplify has six default Gulp tasks to simplify building AMP pages

1. Deletes the contents of the Public directory prior to build 
2. Converts scss => css => minified css => piped into the ```<style amp-custom>``` [tag required by AMP](https://www.ampproject.org/docs/design/responsive/style_pages)
3. Minifies html and includes required amp boilerplate/tags
4. Compresses images
5. Validates AMP using [gulp-amphtml-validator](https://www.ampproject.org/docs/fundamentals/validate#npm-packages-for-ci)
6. Serves project locally  

## Project Process/Structure
* HTML files from src/components are minified and piped to Public 
* images from src/img are compressed and piped to Public/img
* src/style/style.scss is converted to src/style/style.css, minified, and injected into public/index.html
*Do not edit style.css - this file is generated by Gulp*
```
amplify
└───public
    └───img
    └───index.html
└───src
    └───components
        | index.html
    └───img
    └───style
        | style.scss
        | style.css
└──node_modules
| gulpfile.js
| package.json
| README.md
| .gitignore
```

## Tasks
* ```$ gulp``` The default build process.  Deletes the Public directory and then recreates it with the current build.  This ensures that Public doesn't contain leftover files that were not generated by the build.
* ```$ gulp amphtml:validate``` Runs AMP validation test for each HTML file in Public.
* ```$ gulp clean``` Deletes the Public directory.

## Versioning
amplify follows [SemVer](http://semver.org/)

**1.0.0** - create initial gulpfile.js.  update README.

## Dependencies
amplify uses the following packages:
* [browser-sync](https://www.npmjs.com/package/browser-sync)
* [del](https://www.npmjs.com/package/del)
* [gulp](https://www.npmjs.com/package/gulp)
* [gulp-amphtml-validator](https://www.npmjs.com/package/gulp-amphtml-validator)
* [gulp-cssnano](https://www.npmjs.com/package/gulp-cssnano)
* [gulp-htmlmin](https://www.npmjs.com/package/gulp-htmlmin)
* [gulp-image](https://www.npmjs.com/package/gulp-image)
* [gulp-inject-string](https://www.npmjs.com/package/gulp-inject-string)
* [gulp-plumber](https://www.npmjs.com/package/gulp-plumber)
* [gulp-sass](https://www.npmjs.com/package/gulp-sass)

## License
[MIT](https://opensource.org/licenses/MIT)
&copy; 2018 Nick Falcone

## Author
[Nick Falcone](http://nickfalcone.net/)
