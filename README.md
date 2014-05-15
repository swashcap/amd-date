# AMD Date

_AMD-compatible JavaScript date printer._

Use [Ruby-like string-to-time formats](http://rubyinrails.com/2013/09/strftime-format-time-in-ruby/) to get a JavaScript date as a string.

## Usage

1. Use [RequireJS](http://requirejs.org) or a similar module loader.
2. Add _index.js_ to your project.
3.    Load this script in a `define` or `require` (see [RequireJS’s docs](http://requirejs.org/docs/api.html#define)):

    ```javascript
    require(['path/to/amd-date/index'], function(DateHelper) {
      ...
    });
    ```

4.    Inside your module, use the `formatDate` method by passing it a date and desired output format:

    ```javascript
      var myDate = new Date();

      var myFormattedDate = DateHelper.formatDate(myDate, '<h1>%B %d <small>%Y</small></h1>');

      console.log(myFormattedDate);
      // => <h1>May 14 <small>2014<small></h1>
    ```

## ToDos

* Fix `%Z` timezone output
* Internationalization
* Add tests _(help needed!)