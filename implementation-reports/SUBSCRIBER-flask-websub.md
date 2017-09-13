# Flask-WebSub

An implementation of a WebSub hub, publisher and subscriber as a Flask
extension. The implementation is meant to be used as a library that can be
integrated in a larger application.

Implementation Home Page URL: https://github.com/marten-de-vries/Flask-WebSub

Source code repo URL(s): https://github.com/marten-de-vries/Flask-WebSub
* [x] 100% open source implementation

Programming Language(s): Python 3 (with the Flask, Celery and requests
libraries)

Developer(s): [Marten de Vries](https://ma.rtendevri.es)

Answers are:
* [x] Confirmed via websub.rocks (for applicable results)
* [ ] All results are self-reported

## Discovery

* [x] 100: HTTP header discovery - discovers the hub and self URLs from HTTP headers
* [x] 101: HTML tag discovery - discovers the hub and self URLs from the HTML `<link>` tags
* [x] 102: Atom feed discovery - discovers the hub and self URLs from the XML `<link>` tags
* [x] 103: RSS feed discovery - discovers the hub and self URLs from the XML `<atom:link>` tags
* [x] 104: Discovery priority - prioritizes the hub and self in HTTP headers over the links in the body

## Subscription

Note that due to https://github.com/aaronpk/websub.rocks/issues/15, the
subscription reqest connnection actually times out waiting for a 202 response.
This results in an error message being shown. Still, as all the required
processing has happened by then, it does not otherwise hamper running the
tests.

* [x] 1xx: Successfully creates a subscription
* [x] 200: Subscribing to a URL that reports a different rel=self
* [x] 201: Subscribing to a topic URL that sends an HTTP 302 temporary redirect
* [x] 202: Subscribing to a topic URL that sends an HTTP 301 permanent redirect
* [x] 203: Subscribing to a hub that sends a 302 temporary redirect
* [x] 204: Subscribing to a hub that sends a 301 permanent redirect
* [x] 205: Rejects a verification request with an invalid topic URL
* [x] 1xx: Requests a subscription using a secret (optional)
  * Please select the signature method(s) that the subscriber recognizes. All methods listed below are currently acceptable for the hub to choose:
  * [x] sha1
  * [x] sha256
  * [x] sha384
  * [x] sha512
* [x] 1xx: Requests a subscription with a specific `lease_seconds` (optional, hub may ignore)
* [x] Callback URL is unique per subscription (should)
* [x] Callback URL is an unguessable URL (should)
* [x] 1xx: Sends an unsubscription request

## Distribution

* [x] 300: Returns HTTP 2xx when the notification payload is delivered
* [x] 1xx: Verifies a valid signature for authenticated distribution
* [x] 301: Rejects a distribution request with an invalid signature
* [x] 302: Rejects a distribution request with no signature when the subscription was made with a secret

(1xx denotes that you can can use any of the 100-104 tests to confirm this feature)
