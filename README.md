sass-config-manager-mk2
=======================

Put the jumble of configuration variables to order: store all your configuration in a nested hash (Sass map). Access it and manipulate it using handy utils.


Why mark 2
----------

This project is a refactoring of the beautiful [sass-config-manager](https://github.com/sass-projects/sass-config-manager).


### Reasons to fork

1. As of June 2016, **sass-config-manager** was not compatible with **libsass** 3.3.3+.
2. **sass-config-manager** implementation of global/local choice is messy. Using two distinct import endpoints makes the code cleaner.
3. I find customization of namespace, delimiter and other options to be needless features. They are removed in **mk2** in order to make the source simpler. **mk2** only uses two variables: `$-config-storage` and `$-config-storage-default` to store user and default values respectively.
4. **sass-config-manager** uses a crazy Grunt pipeline. I find it completely unnecessary because Sass supports `@import`.
5. All variables, functions and mixins defined by **mk2** predictably start only with `config-` and `-config-`. This reduces the risk of naming collisions.


### Design decisions

* **mk2** is written with the indentation-driven `.sass` syntax. Way less visual noise! You can still import it into `.scss` code.
* The `config-get` mixin and `config-set` function have been removed for simplicity. Use the `config-get` function and `config-set` mixin.
* Private variable, function and mixin names start with a dash.

-- Andrey Mikhaylov ([@lolmaus](https://github.com/lolmaus/))


Roadmap
-------

> #### Legend
>
> :white_circle: -- not implemented yet, planned  
> :radio_button: -- in progress (leaf) or partially implemented (branch)  
> :black_circle: -- implemented   
> :no_entry:     -- blocked, has to be figured out

* :white_circle: Installation and usage info in the readme.
* :white_circle: Tests using [True](http://oddbird.net/true/) and [Mocha](https://mochajs.org/).
* :white_circle: Inline documentation using [SassDoc](http://sassdoc.com/).
* :white_circle: Bower package.
* :white_circle: npm package.
* :white_circle: [Eyeglass](https://github.com/sass-eyeglass/eyeglass) support.





Credits
-------

Contains code from [sass-config-manager](https://github.com/sass-projects/sass-config-manager) created by Daniel Bannert ([@prisis](https://github.com/prisis)) and [contributors](https://github.com/sass-projects/sass-config-manager/graphs/contributors).


License
-------

MIT license (see LICENSE.md).
