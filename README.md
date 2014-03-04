Heroku buildpack: Yeoman
=========================

This is a [Heroku buildpack](http://devcenter.heroku.com/articles/buildpacks) for yeoman apps.
It uses [Bower](https://github.com/bower/bower), [Grunt](gruntjs.com), [NPM](http://npmjs.org/) and [SCons](http://www.scons.org/).

Usage
-----

Work with yeoman locally as you normally would. Push to Heroku with this buildpack, `bower install` and `grunt` will automatically be run. This buildpack will try to mirror the typical local yeoman workflow on Heroku.

    $ npm install -g yo grunt-cli bower
    $ npm install -g generator-webapp
    $ yo webapp
    $ bower install
    $ grunt

    $ heroku create --buildpack https://github.com/eugeniodepalo/heroku-buildpack-yeoman.git

    $ git push heroku master

    -----> Heroku receiving push
    -----> Fetching custom buildpack
    -----> Installing dependencies with npm 1.0.8
           express@2.1.0 ./node_modules/express
           ├── mime@1.2.2
           ├── qs@0.3.1
           └── connect@1.6.2
           Dependencies installed
    -----> Found bower.json, running bower install
    -----> Found Compass in package.json, installing it
    -----> Found Gruntfile, running grunt task

Done. Your yeoman app should work.

TODO
----
* Vendor phantomjs
