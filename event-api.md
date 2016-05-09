# Event API

The Event API handles POST requests with arbitrary JSON payloads from external sources and relays them as event messages to internal Emma services.

The private repo containing the Event API's implementation is
[`emmadev/external-events`](https://github.com/emmadev/external-events).

The endpoint for the Event API is `https://events.e2ma.net/v1/<account>/events/`.

The endpoint accepts POST requests with valid JSON.  However, the payload must include a valid email address currently associated with a contact in user’s audience to trigger workflow (i.e., `"email": "user@acme.org"`). The request must also include an Authorization header consisting of a user's public API key as username, private key as password, encoded in [basic auth](https://en.wikipedia.org/wiki/Basic_access_authentication#Client_side) format.  A user can generate API keys from their Emma account in **Account Settings** under the *API Key* tab.

For example, setting up the headers for your POST request might look as follows:

```
const data = {
  "event": "newsletter signup",
  "email": "user@acme.com"
});
const body = JSON.stringify(data);

const username = YOUR_PUBLIC_KEY;
const password = YOUR_PRIVATE_KEY;
const credentials = new Buffer(username + ":" + password).toString("base64");

const headers = {
  "Authorization": "Basic " + credentials,
  "Content-Type": "application/json",
  "Content-Length": body.length
};
```


## Workflows

Automation workflows can be ...

* triggered by events passed through the event API 
* configured using the “Custom API Event” trigger type in the Automation workflow builder
* filtered by up to 5 criteria of any given event (e.g. “event-name” equals “purchase,” “purchase-amount” is greater than “100,” and “shipping method” equals “overnight”)


## Dynamic content

Events can provide dynamic content for mailings.

For example, we could have a mailing show image A if *shipping method* is **overnight** and image B if *shipping method* is **standard mail**. 

More information on dynamic content can be found [here](http://support.e2ma.net/Resource_Center/Account_how-to/How_to_use_dynamic_content).

Unlike data from a contact record, data from events is prefixed by `event:`.

* Dynamic data from contact record: `[% if "member:city" == "Nashville" %]`)
* Dynamic data from event: `[% if "event:shipping-method" == "overnight" %]`).
