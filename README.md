# amplify

Build AMP Pages quickly. Minify/compress files. Validation from the command line.
[Learn more about AMP](https://www.ampproject.org/learn/overview/)

## Getting Started

```sh
$ git clone https://github.com/nickFalcone/amplify.git
$ cd amplify
$ npm install
$ gulp
```

## What amplify does
amplify has four default Gulp tasks to simplify building AMP pages

1. converts your scss => css => minified css => injected into ```<style amp-custom>``` [tag required by AMP](https://www.ampproject.org/docs/design/responsive/style_pages)
2. minifies html, and includes required amp boilerplate/tags
3. compresses images
4. validates AMP using [gulp-amphtml-validator](https://www.ampproject.org/docs/fundamentals/validate#npm-packages-for-ci)

amplify will then serve your project locally from the Public directory.  It also watches your HTML/SCSS files for changes.

## Project Structure
Running ```$ gulp``` will create the ```public``` directory.
HTML files from ```src/components``` are minified and piped to ```public``` directory
images from ```src/img``` are minified and piped to ```public/img```
```src/style/style.scss``` is converted to ```src/style/style.css```, minified, and injected into ```public/index.html```
***Do not edit style.css - this file is generated by Gulp***

```
amplify
└───public
│   └───img
│   └───index.html
───node_modules
└───src
│   └───components
        | index.html
│   └───img
│   └───style
        | style.scss
        | style.css
| gulpfile.js
| package.json
| README.md
| .gitignore
```
## Versioning

amplify follows [SemVer](http://semver.org/) for versioning
**1.0.0** - create initial gulpfile.js.  update README.

## License
[MIT](https://opensource.org/licenses/MIT)
&copy; 2018 Nick Falcone

## Author
[Nick Falcone](http://nickfalcone.net/)
