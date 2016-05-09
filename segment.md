# Segment.com integration

For context, it may be useful to read [Active Campaign's description](http://www.activecampaign.com/blog/share-contact-data-with-other-apps/) of their integration with Segment.

Segment provides [a list of integration partners](https://segment.com/integrations) and it's worth viewing those in the **email** category.  For example, see MailChimp's [integration docs](https://segment.com/docs/integrations/mailchimp/) to see how you can add people to your Mailchimp list with a single identify call.


## Implementation

We're going to implement a [direct integration](https://segment.com/docs/partners/direct-integration/#2-build-an-endpoint-to-receive-customer-data) for [Segment.com](https://segment.com), leveraging the work that's been done for Emma's general purpose [Events API](https://github.com/emmadev/external-events).

For a direct integration, we need to setup a dedicated endpoint (`https://events.e2ma.net/v1/segment`). This endpoint will receive event notifications, proxied by Segment, but originally issued by client libraries of Segment users.  Our endpoint will be defined via the AWS API Gateway, which forwards requests to a dedicated Lambda function. Lambda takes care of horizontal scaling. It provides high availabilty, low latency, and scalability by default.

After authenticating requests with a [custom authorizer](https://aws.amazon.com/jp/blogs/compute/introducing-custom-authorizers-in-amazon-api-gateway/), our Lambda function will proxy inbound events to an appropriate SNS topic for further processing (e.g., triggering workflows, etc.).


## Resources 

* the segment [spec](https://segment.com/docs/spec/)

* [details on the endpoint needed to support a direct integration](https://segment.com/docs/partners/direct-integration/#2-build-an-endpoint-to-receive-customer-data)

* [details on how to streamline the Segment connect setup for users](https://segment.com/docs/partners/enable-with-segment/)

* [details on how to setup a webhook integration](https://segment.com/docs/integrations/webhooks/), for experimenation and testing

* [go client library](https://segment.com/docs/libraries/go/) for sending event
  notifications



