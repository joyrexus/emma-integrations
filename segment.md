# Segment.com integration

We're going to implement a [direct integration](https://segment.com/docs/partners/direct-integration/#2-build-an-endpoint-to-receive-customer-data) for [Segment.com](https://segment.com), leveraging the work that's been done for Emma's general purpose [Events API](https://github.com/emmadev/external-events).

For context, it may be useful to read [Active Campaign's description](http://www.activecampaign.com/blog/share-contact-data-with-other-apps/) of their integration with Segment.

Segment provides [a list of integration partners](https://segment.com/integrations) and it's worth viewing those in the **email** category.  For example, see MailChimp's [integration docs](https://segment.com/docs/integrations/mailchimp/) to see how you can add people to your Mailchimp list with a single identify call.


## Resources 

* the segment [spec](https://segment.com/docs/spec/)

* [details on the endpoint needed to support a direct integration](https://segment.com/docs/partners/direct-integration/#2-build-an-endpoint-to-receive-customer-data)

* [details on how to streamline the Segment connect setup for users](https://segment.com/docs/partners/enable-with-segment/)

* [details on how to setup a webhook integration](https://segment.com/docs/integrations/webhooks/), for experimenation and testing

* [go client library](https://segment.com/docs/libraries/go/) for sending event
  notifications



