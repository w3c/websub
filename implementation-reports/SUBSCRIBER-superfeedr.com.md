# superfeedr.com

Superfeedr will act as a subscriber when provided with a topic to poll on behalf of one of our customers.

Implementation Home Page URL: https://superfeedr.com

Answers are:
* [X] Confirmed via websub.rocks (for applicable results)
* [ ] All results are self-reported

## Discovery

* [X] 100: HTTP header discovery - discovers the hub and self URLs from HTTP headers
* [X] 101: HTML tag discovery - discovers the hub and self URLs from the HTML `<link>` tags
* [X] 102: Atom feed discovery - discovers the hub and self URLs from the XML `<link>` tags
* [X] 103: RSS feed discovery - discovers the hub and self URLs from the XML `<atom:link>` tags
* [X] 104: Discovery priority - prioritizes the hub and self in HTTP headers over the links in the body

## Subscription

* [X] 1xx: Successfully creates a subscription
* [X] 200: Subscribing to a URL that reports a different rel=self
* [X] 201: Subscribing to a topic URL that sends an HTTP 302 temporary redirect
* [X] 202: Subscribing to a topic URL that sends an HTTP 301 permanent redirect
* [0] 203: Subscribing to a hub that sends a 302 temporary redirect
Not currently supported by Superfeedr. on roadmap
* [0] 204: Subscribing to a hub that sends a 301 permanent redirect
Not currently supported by Superfeedr. on roadmap
* [0] 205: Rejects a verification request with an invalid topic URL
The test fails... i have to look into this
* [X] 1xx: Requests a subscription using a secret (optional)
  * Please select the signature method(s) that the subscriber recognizes. All methods listed below are currently acceptable for the hub to choose:
  * [X] sha1
  * [ ] sha256
  * [ ] sha384
  * [ ] sha512
* [X] 1xx: Requests a subscription with a specific `lease_seconds` (optional, hub may ignore)
* [X] Callback URL is unique per subscription (should)
* [?] Callback URL is an unguessable URL (should)
We're using sequences of numbers... BUT they're probably not unguessable by brute force. On roadmap
* [X] 1xx: Sends an unsubscription request

## Distribution

* [X] 300: Returns HTTP 2xx when the notification payload is delivered
* [X] 1xx: Verifies a valid signature for authenticated distribution
* [X] 301: Rejects a distribution request with an invalid signature
* [X] 302: Rejects a distribution request with no signature when the subscription was made with a secret

(1xx denotes that you can can use any of the 100-104 tests to confirm this feature)
