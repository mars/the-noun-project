The Noun Project
================

[![npm Module](https://img.shields.io/npm/v/@mars/the-noun-project.svg)](https://www.npmjs.com/package/@mars/the-noun-project)

Node.js wrapper for The Noun Project's API

Installation
------------
Simply add to your project with
````bash
npm install --save @mars/the-noun-project
````

In your project file:
````javascript
var NounProject = require('@mars/the-noun-project'),
nounProject = new NounProject({
    key: 'foo',
    secret: 'bar'
});
````
You can get your keys from [The Noun Project developer's page](https://thenounproject.com/developers/).

Usage
-----
See [The Noun Project API Explorer](http://api.thenounproject.com/explorer) for more information on the endpoints available.

The query string `options` object is optional and can be omitted. See the tests for more information.


````javascript
nounProject.getIconsByTerm('goat', {limit: 5}, function (err, data) {
    if (!err) {
        console.log(data.icons);
    }
});
````
**or**
````javascript
nounProject.getIconsByTerm('goat', function (err, data) {
    if (!err) {
        console.log(data.icons);
    }
});
````
