# Projects

Suggestions and ideas for Emma's nascent integrations team.


## API docs

* Revise and expand the [API docs](http://api.myemma.com/index.html). See the [`gh-pages`](https://github.com/myemma/emma-api-documentation/tree/gh-pages) branch of the [repo](https://github.com/myemma/emma-api-documentation).

* Compare with API docs of other vendors:
  * [MailChimp](http://developer.mailchimp.com/documentation/mailchimp/)
  * [SendGrid](https://sendgrid.com/docs/API_Reference/index.html)
  * [Campaign Monitor](https://www.campaignmonitor.com/api/getting-started/)

* Compare API doc/testing tools [Apiary vs ReadMe vs Gelato](http://stackshare.io/stackups/apiary-vs-readme-io-vs-gelato-io)

* Review API prototyping tutorials:
  * [Quickly Prototype APIs with Apiary](https://sendgrid.com/blog/quickly-prototype-apis-apiary/)
  * [Building APIs with Swagger](http://radar.oreilly.com/2015/09/building-apis-with-swagger.html)


## API clients

Create a golang client for the Public API mirroring the features of the [node](https://github.com/nathanpeck/emma-sdk) and [python](https://github.com/myemma/EmmaPython) clients.

Consider creating [github-hosted project pages](https://pages.github.com) for official Emma clients libs. See [createsend client lib](http://campaignmonitor.github.io/createsend-python/) as an example.


## Segment integration

Implement a [direct integration](https://segment.com/docs/partners/direct-integration/#2-build-an-endpoint-to-receive-customer-data) with [Segment](https://segment.com).

#### Resources 

* Segment [integrations list](https://segment.com/integrations) -- see the
  **email** category

* Segment [spec](https://segment.com/docs/spec/)

* MailChimp's [integration docs](https://segment.com/docs/integrations/mailchimp/)

* [Overview](http://www.activecampaign.com/blog/share-contact-data-with-other-apps/) of Active Campaign's integration.


## Slack app

Create [a Slack app](https://api.slack.com/slack-apps) providing Slash commands for key endpoints and incoming webhooks for event notification.

See the [MailChimp](https://slack.com/apps/A0F82E726-mailchimp) and [Intercom](https://slack.com/apps/A0F81R6LF-intercom) Slack apps for the basic model.


## Other

* Review [REST hook patterns](http://resthooks.org/docs/).  REST hooks are a set of patterns for implementing subscription-based webhooks. See [this flask-based example](https://github.com/zapier/resthooks).

* Evaluate potential use of [rehook](https://github.com/jstemmer/rehook) for dispatching, logging, and metrics.

* Evaluate API doc/testing options
  * [yaag](https://github.com/betacraft/yaag), an API doc generator for golang web services.
  * [silk](https://medium.com/@matryer/introducing-silk-markdown-driven-api-tests-1f8cfb0ef99a#.roley2jzv) 

