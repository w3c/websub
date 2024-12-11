# FeedMail

Implementation Home Page URL: https://feedmail.org

Source code repo URL(s) (optional):
* [ ] 100% open source implementation

Programming Language(s): Rust

Developer(s): [Kevin Cox](https://kevincox.ca)

Answers are:
* [ ] Confirmed via websub.rocks (for applicable results)
* [x] All results are self-reported

## Discovery

* [x] 100: HTTP header discovery - discovers the hub and self URLs from HTTP headers
* [ ] 101: HTML tag discovery - discovers the hub and self URLs from the HTML `<link>` tags
* [x] 102: Atom feed discovery - discovers the hub and self URLs from the XML `<link>` tags
* [x] 103: RSS feed discovery - discovers the hub and self URLs from the XML `<atom:link>` tags
* [x] 104: Discovery priority - prioritizes the hub and self in HTTP headers over the links in the body

## Subscription

* [x] 1xx: Successfully creates a subscription
* [ ] 200: Subscribing to a URL that reports a different rel=self
  * Note: Due to concerns about misconfigured feeds FeedMail currently ignores WebSub where the self link differs substantially from the feed URL and falls back to polling.
* [x] 201: Subscribing to a topic URL that sends an HTTP 302 temporary redirect
* [x] 202: Subscribing to a topic URL that sends an HTTP 301 permanent redirect
* [x] 203: Subscribing to a hub that sends a 302 temporary redirect
* [x] 204: Subscribing to a hub that sends a 301 permanent redirect
* [x] 205: Rejects a verification request with an invalid topic URL
* [ ] 1xx: Requests a subscription using a secret (optional)
  * Please select the signature method(s) that the subscriber recognizes. All methods listed below are currently acceptable for the hub to choose:
  * [ ] sha1
  * [ ] sha256
  * [ ] sha384
  * [ ] sha512
* [x] 1xx: Requests a subscription with a specific `lease_seconds` (optional, hub may ignore)
* [x] Callback URL is unique per subscription (should)
* [x] Callback URL is an unguessable URL (should)
* [ ] 1xx: Sends an unsubscription request

## Distribution

* [x] 300: Returns HTTP 2xx when the notification payload is delivered
* [ ] 1xx: Verifies a valid signature for authenticated distribution
* [x] 301: Rejects a distribution request with an invalid signature
* [ ] 302: Rejects a distribution request with no signature when the subscription was made with a secret

(1xx denotes that you can can use any of the 100-104 tests to confirm this feature)
