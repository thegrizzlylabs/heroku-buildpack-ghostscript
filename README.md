# Heroku Buildpack for Ghostscript

Currently installs Ghostscript 10.08.0 on Heroku, built from source (Artifex no longer publishes prebuilt Linux binaries), so deploys take a few minutes longer.

## Install

    # Use heroku-buildpack-multi
    $ cd /path/to/your-app
    $ heroku config:add BUILDPACK_URL=https://github.com/ddollar/heroku-buildpack-multi.git

    # Create a .buildpacks file with including ghostscript
    $ cd /path/to/your-app
    $ cat .buildpacks
    https://github.com/heroku/heroku-buildpack-ruby.git
    https://github.com/bvirlet/heroku-buildpack-ghostscript.git

    # Push changes to deploy
    $ git push
