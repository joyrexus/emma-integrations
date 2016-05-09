# javascript

A list of conventions and resources for the integrations team.


## learn hapi

We utilize [hapijs](http://hapijs.com) for internal web services.

* [intro tutorial](http://hapijs.com/tutorials)
* [nearform tutorial](http://www.nearform.com/nodecrunch/building-apis-hapi-js/)
* [boilerplate quickstart](https://github.com/emmadev/architecture/blob/master/docs/hapi-boilerplate-quick-start.md)

Take note of the [`hapi-auth` plugin](https://github.com/emmadev/hapi-auth#hapi-auth) for handling [user authentication and authorization](https://medium.com/@poeticninja/authentication-and-authorization-with-hapi-5529b5ecc8ec#.r47s22gls) in your hapi services at Emma.


## style guides

We embrace the conventions espoused in the following style guides.

* [hapijs](http://hapijs.com/styleguide)
* [airbnb](https://github.com/airbnb/javascript)


## jsdoc comments

We strongly recommend commenting your code with jsdoc comments.

* [get started](http://usejsdoc.org/about-getting-started.html)
* include [examples](http://usejsdoc.org/tags-example.html)
* use [documentation.js](https://github.com/documentationjs/documentation#documentation-1) for generating docs
* [example usage](https://github.com/simple-statistics/simple-statistics/blob/master/src/median_sorted.js)


## testing

* [use tape](http://www.macwright.org/2014/03/11/tape-is-cool.html)
* see examples in [turf.js](https://github.com/Turfjs/turf/blob/master/packages/turf-along/test.js) and [simple-statistics.js](https://github.com/simple-statistics/simple-statistics/blob/master/test/geometric_mean.test.js)
* [know when to throw](http://www.nearform.com/nodecrunch/10-tips-coding-node-js-3-know-throw-2/)
* see an [example of testing an http request](http://robjoh.com/testing-a-server-request-with-hapi-and-lab/) with hapi, lab, and sinon
* but [use nock](https://github.com/node-nock/nock#nock) instead of sinon
* see [intro nock article](http://jakepruitt.com/2014/11/13/nock.html)


## error handling

* return [error objects](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Error#Examples), [not strings](http://www.devthought.com/2011/12/22/a-string-is-not-an-error/)


## promises

* use [promises](http://alexperry.io/node/2015/03/25/promises-in-node.html) for
async control flow
* avoid [anti-patterns](https://pouchdb.com/2015/05/18/we-have-a-problem-with-promises.html)
