Public Data Platform
====================

<<<<<<< HEAD
This is the documentation repository for the Public Data Platform API. It is a separate effort from Qu, the software that powers this API. That documentation lives [here](http://cfpb.github.io/qu/).

Check out the [gh-pages view](https://github.cfpb.gov/pages/data-platform/public-data-platform.io/). 

Thanks to the eregs team and their documentation work for starting us off with a great codebase.
=======


This is the documentation repository for the Home Mortgage Disclosure Act (HMDA) dataset served by the Public Data Platform API.
Check out this API documentation at https://cfpb.github.io/api/hmda/

It is a separate effort from [Qu](https://github.com/cfpb/qu), the software that powers this API.
Qu's documentation lives at http://cfpb.github.io/qu/.

Thanks to the [eRegs](https://github.com/cfpb/regulations-core) team and their documentation work for
starting us off with a great codebase.

You can use [DOCter](https://github.com/cfpb/DOCter) to build documentation sites similar to this one.
>>>>>>> 9a10e46081224574bc5ce0462dd8e35c4e210f35

## Using JavaScript and Bower

If you are going to work on the JavaScript for this site, you need to do the following:

* Run `npm install -g bower` to install Bower.
* Run `npm install -g grunt-cli` to install Grunt.
* Run `npm install` in the directory to install other tools.
* Run `bower install` to install dependencies.

After changing the JavaScript, run `grunt` to rebuild the minified JS.


