# Projects

Suggestions and ideas for Emma's nascent integrations team.


## API docs

* Revise and expand the [API docs](http://api.myemma.com/index.html). See the [`gh-pages`](https://github.com/myemma/emma-api-documentation/tree/gh-pages) branch of the [repo](https://github.com/myemma/emma-api-documentation).

* Compare with API docs of other vendors:
  * [Campaign Monitor](https://www.campaignmonitor.com/api/getting-started/)
  * [MailChimp](http://developer.mailchimp.com/documentation/mailchimp/)
  * [SendGrid](https://sendgrid.com/docs/API_Reference/index.html)

* Compare API doc/testing tools [Apiary vs ReadMe vs Gelato](http://stackshare.io/stackups/apiary-vs-readme-io-vs-gelato-io)


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
