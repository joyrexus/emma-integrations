# Emma Integrations

We at Emma are in the process of setting up a new Integrations Engineering
Team.  Most of us are new to the company, still getting oriented.  This is an initial attempt at an overview of Emma's current integration landscape along with some suggestions for future integration tasks.


# Options

There are two principal resources for developing third-party integrations with
Emma, viz., Emma's [Public API](http://api.myemma.com/index.html) and an internally available [Integration Service](https://github.com/emmadev/eda-integrations).

## Public API

Emma’s platform is accessible through a public API. This is a JSON/REST API that enables clients to manage member mailing lists and access mailing response data.

In particular, the API enables clients to ...

* import, edit, and delete members
* organize members into groups
* search for members
* retrieve past mailings
* control status of pending mailings
* access mailing response info (opens, clicks, shares, opt-outs)

The API contains [endpoints for the following resources](http://api.myemma.com/index.html#api-calls-by-category):

* fields
* groups
* mailings
* members
* response
* searches
* signup forms
* triggers
* webhooks

The API also provides notifications via webhooks for the following mailing response events:

* member ...
  * signup
  * optout

* message ...
  * open
  * click
  * share
  * share click
  * forward

It also provides notifications for the following account-level events:

* mailing finish
* import finish
* member ...
  * create / update / delete
  * add to group
  * remove from group
  * status update
* group create / update / delete
* field create / update / delete

[This document](http://api.myemma.com/api/external/webhooks.html) describes how to activate webhook notifications for a particular account.

 
## Integration Service

See the [`eda-integrations`](https://github.com/emmadev/eda-integrations) repo. Emma's Integration Service consists of a [hapi](http://hapijs.com)-based http server as well as a few python-based event-driven handlers. The service can be used for contact syncing, event notification via webhooks, and serving up content blocks to Emma's frontend editor.

For an overview of the service and a description of how to use it for contact syncing, see [this document](https://github.com/emmadev/eda-integrations/blob/master/docs/ac-overview.md).


# Todo

* Review [REST hook patterns](http://resthooks.org/docs/).  REST hooks are a set of patterns for implementing subscription-based webhooks. See [this flask-based example](https://github.com/zapier/resthooks).

* Evaluate potential use of [rehook](https://github.com/jstemmer/rehook) for dispatching, logging, and metrics.

* Revise and expand the [pubic API docs](http://api.myemma.com/index.html). See the [`gh-pages`](https://github.com/myemma/emma-api-documentation/tree/gh-pages) branch of the [repo](https://github.com/myemma/emma-api-documentation).

* Create a golang client mirroring the features of the
  [node](https://github.com/nathanpeck/emma-sdk) and
  [python](https://github.com/myemma/EmmaPython) clients.

* Create [a Slack app](https://api.slack.com/slack-apps) providing Slash commands for key endpoints and incoming webhooks for event notification.
