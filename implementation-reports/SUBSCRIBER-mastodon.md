# Mastodon

Implementation Home Page URL: https://mastodon.social/

Source code repo URL(s) (optional):
* [x] 100% open source implementation

Programming Language(s): Ruby

Developer(s): [Eugen Rochko](https://github.com/Gargron)

Answers are:
* [ ] Confirmed via websub.rocks (for applicable results)
* [x] All results are self-reported

Note: Answers were reported in IRC by Eugen Rochko and transcribed to this report by Aaron Parecki. https://chat.indieweb.org/social/2017-07-12#t1499876947598000

## Discovery

* [ ] 100: HTTP header discovery - discovers the hub and self URLs from HTTP headers
* [ ] 101: HTML tag discovery - discovers the hub and self URLs from the HTML `<link>` tags
* [x] 102: Atom feed discovery - discovers the hub and self URLs from the XML `<link>` tags
* [ ] 103: RSS feed discovery - discovers the hub and self URLs from the XML `<atom:link>` tags
* [ ] 104: Discovery priority - prioritizes the hub and self in HTTP headers over the links in the body

## Subscription

* [x] 1xx: Successfully creates a subscription
* [ ] 200: Subscribing to a URL that reports a different rel=self
* [ ] 201: Subscribing to a topic URL that sends an HTTP 302 temporary redirect
* [ ] 202: Subscribing to a topic URL that sends an HTTP 301 permanent redirect
* [ ] 203: Subscribing to a hub that sends a 302 temporary redirect
* [ ] 204: Subscribing to a hub that sends a 301 permanent redirect
* [x] 205: Rejects a verification request with an invalid topic URL
* [ ] 1xx: Requests a subscription using a secret (optional)
  * Please select the signature method(s) that the subscriber recognizes. All methods listed below are currently acceptable for the hub to choose:
  * [x] sha1
  * [ ] sha256
  * [ ] sha384
  * [ ] sha512
* [x] 1xx: Requests a subscription with a specific `lease_seconds` (optional, hub may ignore)
* [x] Callback URL is unique per subscription (should)
* [ ] Callback URL is an unguessable URL (should)
* [x] 1xx: Sends an unsubscription request

## Distribution

* [x] 300: Returns HTTP 2xx when the notification payload is delivered
* [x] 1xx: Verifies a valid signature for authenticated distribution
* [x] 301: Rejects a distribution request with an invalid signature
* [x] 302: Rejects a distribution request with no signature when the subscription was made with a secret
