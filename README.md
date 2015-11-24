# Cyanide & Magenta

This is the late 2015 rebuild of [Caitlynmayers.com](www.caitlynmayers.com)/[Cyanide & Magenta](www.cyanideandmagenta.com). 

## Dependencies
The site is built using the [generator-jekyll](https://www.npmjs.com/package/generator-jekyllized) package.

## Known Issues
1. A few dependencies didn't install correctly. Bundler and Yo needed to be installed post-install of the package, Gulp Sass didn't work correctly, and the default pagination settings created in the config.yml file caused some pagination errors to be thron when attempting to build the project. Followed [these steps](https://github.com/sondr3/generator-jekyllized/issues/103) in order to fix these issues.

## Getting started

### Installation
* **Install dependencies:** Bundler `>1.10`, Node.js `>4.2`, Gulp `>4.0`, Ruby `>1.9` and Yo `>1.5.0`
* **Gulp:** Since the beta is running Gulp 4.0 you need to install `gulp-cli`:
  `npm install gulpjs/gulp-cli#4.0 -g`
* **Jekyllized:** Then install Jekyllized: `npm install
    generator-jekyllized@1.0.0-beta.3 -g`
* **Scaffold:** Run `yo jekyllized` in the directory you want your site to
  scaffold in
* **Start:** Run `gulp` and watch the magic unfold and/or look at the [FAQ][faq]
  for more options.

## Usage

#### `gulp [--prod]`

Running this will build your assets, copy your images and fonts, build your site and start a BrowserSync session in your browser. Any change you make to (pretty much) any file in the `src` directory will have the associated change be automatically updated, built and pushed to your browser. By default all optimizations are disabled, and source maps are enabled for easy debugging.

When you run the command with `--prod` you are changing into production
settings. It's mostly the same as the default, however all your CSS and JS are minifed, gzipped, cache busted and your HTML is minified as well and source maps are disabled. Use when you're done developing locally to verify that nothing is broken and that everything works.

#### `gulp build [--prod]`

This command is identical to the `gulp` command, the only difference is that it doesn't create a BrowserSync session in your browser.

#### `gulp deploy`

When you're done developing and have built your site with either `gulp --prod` or `gulp build --prod` you can deploy your site to either Amazon S3, Github Pages or with Rsync.

> Amazon S3 and Rsync

If you chose either of these two, you'll have a `[rsync/aws]-credentials.json` file in your root folder that you have to fill out. It should be pretty self explanatory, however, if you need any help with configuring it, you should check out either the [`gulp-awspublish`][awspublish] repo or [`gulp-rsync`][rsync] repo for help.

> Github Pages

If you chose to upload to Github Pages there's no configuration besides starting a git repo in your folder, setting an `origin` remote repo and run `gulp deploy`. Your site will be automatically pushed to Github. See the [FAQ][faq] for configuring personal repos vs project repos.

#### `gulp check`

Lints your JavaScript files using ESLint with XO Space settings and run `jekyll doctor` to look for potential errors.

#### `gulp clean`

Deletes your assets from their `.tmp` directory as well as in `dist` and deletes any gzipped files.

#### `gulp rebuild`

Only run when you need to do a full rebuild! This will delete your built site and all the assets with it.

### Subtasks

All of the commands listed above are the main commands, and are composed of other smaller commands that have a small job that they do. You can find all the command by running `gulp --tasks`, and look in the [gulpfile][gulpfile] for what they do. All are commented about what they do.