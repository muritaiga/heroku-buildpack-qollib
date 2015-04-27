Heroku buildpack: qollib
=======================

This is a [Heroku buildpack](http://devcenter.heroku.com/articles/buildpacks) for using qollib in your project.  
It doesn't do anything else, so to actually compile your app you should use [heroku-buildpack-multi](https://github.com/ddollar/heroku-buildpack-multi) to combine it with a real buildpack.

Usage
-----
To use this buildpack, you should prepare .buildpacks file that contains this buildpack url and your real buildpack url.  

    $ ls
    .buildpacks
    ...
    
    $ cat .buildpacks
    https://github.com/muritaiga3/heroku-buildpack-apt
    https://github.com/muritaiga3/heroku-buildpack-qollib
    https://github.com/heroku/heroku-buildpack-ruby

    $ heroku create --buildpack https://github.com/ddollar/heroku-buildpack-multi

    $ git push heroku master
    ...
