PHPUnit script invoker
======================

Many PHP projects now supply [PHPUnit][1] via `require-dev` in composer.
This means that to run PHPUnit, you often have to supply a full path
to the local `phpunit` binary.

This package is intended to be installed globally, and supplies you with a
`phpunit` script as well.

This script will automatically find a `composer.json` in your current path
or one of its parents, and find the correct "local" phpunit script and
runs it for you.

In addition to that, it will also attempt to find `phpunit.xml` or
`phpunit.xml.dist` and change the working directory to that path before
running the real `phpunit` script.

This means that using this script, you can just invoke `phpunit` from wherever
you are in your project, and it will run it correctly.


Installation
------------

    composer global require evert/phpunit-bin

Make sure that after you run that, your global composer `bin` directory is
in your `$PATH`. This is usually `~/.composer/vendor/bin`.


[1]: https://phpunit.de/

