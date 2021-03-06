[![Build Status](https://travis-ci.org/weblogng/angular-weblogng.svg?branch=master)](https://travis-ci.org/weblogng/angular-weblogng)

# angular-weblogng #

angular-weblogng is an AngularJS module for the [WeblogNG Javascript Client library](https://github.com/weblogng/weblogng-client-javascript)

angular-weblogng provides:
 
* automatic measurement and reporting of application load time
* automatic measurement and reporting of requests made with the [$http service](https://docs.angularjs.org/api/ng/service/$http)
* automatic measurement of the number of active users
* easy access to the [WeblogNG Javascript Client library](https://github.com/weblogng/weblogng-client-javascript)

## Installation ##

Using Bower:

    bower install angular-weblogng --save

Or grab the [source](https://github.com/weblogng/angular-weblogng/blob/master/dist/angular-weblogng.js) ([minified](https://github.com/weblogng/angular-weblogng/blob/master/dist/angular-weblogng.min.js)).

## Usage ##

The WeblogNG module can be integrated into an application by:

1. include the angular-weblogng.js and WeblogNG Logger scripts in your application, e.g. bower_components/angular-weblogng/dist/angular-weblogng.js and bower_components/weblogng-logger/release/logger.js 
2. define the 'weblogng' module as one of the application's dependencies
3. declare the 'weblogngConfig' constant

Example app configuration with the WeblogNG module:

    angular.module('yourAppModule', [
        'weblogng'
      ])
      .constant('weblogngConfig', {
        apiKey: 'your api key',
        options: {
          publishNavigationTimingMetrics: true,
          publishUserActive: true,
          application: 'your application name'
        }
      })
      
## Documentation ##

Detailed documentation is available at [docs.weblogng.com](http://docs.weblogng.com/en/latest/client-library-angular-weblogng.html)

## Contributing ##

We'd love to consider your contribution! Please:

* Provide a comprehensive suite of tests for your fork.
* Have a clear and documented rationale for your changes.
* Package these up in a pull request.

We'll do our best to help you out with any contribution issues you may have.

## Developing ##

Use the `grunt watch` command to execute the build continuously during development.

## License ##

MIT. See `LICENSE.txt` in this directory.
