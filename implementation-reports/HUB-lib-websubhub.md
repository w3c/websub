# lib-websubhub v0.5.0 in-memory reference hub

Implementation Home Page URL: https://github.com/ayeshLK/lib-websubhub/releases/tag/v0.5.0

Source code repo URL(s) (optional): https://github.com/ayeshLK/lib-websubhub
* [x] 100% open source implementation

Programming Language(s): Go

Developer(s): [Ayesh Almeida](https://github.com/ayeshLK)

Answers are:
* [x] Confirmed via websub.rocks (for applicable results)
* [x] All results are self-reported

The tested implementation is the `lib-websubhub` v0.5.0 framework composed
with its in-memory reference application. The framework supplies WebSub
protocol mechanics; the application supplies topic and subscription state,
lease expiry, content retrieval, fan-out, and delivery scheduling.

## Subscription

* [x] 100: Supports subscriptions with `hub.mode`, `hub.topic` and `hub.callback`
* [x] 101: Supports subscriptions with `hub.mode`, `hub.topic`, `hub.callback` and `hub.secret`
* [x] 102: Ignores unrecognized parameters in the subscription request
* [x] 103: Allows subscribers to re-request active subscriptions before they expire
* [x] 104: Supports unsubscription requests
* [x] 1xx: Sends a properly formatted verification request for subscribing and unsubscribing
* [x] Allows subscribers to request a specific lease duration

The framework accepts a positive whole-second requested lease, applies the
application-configured maximum, and reports the effective lease during intent
verification. The reference application persists and expires that lease.

(1xx denotes that you can can use any of the 100-104 tests to confirm this feature)

## Distribution

* [x] 100: Sends a notification with a matching content-type of the topic URL
* [x] 100: Sends a notification with the full contents of the topic
* [x] 101: Sends a notification with a valid signature
  * Please select the signature method(s) that the hub uses to sign requests
  * [ ] sha1
  * [x] sha256
  * [ ] sha384
  * [ ] sha512
* [ ] Sends only a diff of the topic URL for Atom or RSS feeds

The implementation sends the complete topic representation rather than an
Atom or RSS diff. websub.rocks tests 105 and 106 also confirmed exact plaintext
and JSON content delivery.

## Test notes

Tests 100 through 106 were run against an ephemeral HTTPS deployment on
2026-08-21. Temporary websub.rocks topics were registered with the reference
application before subscription. Content updates were then triggered through
the project's optional publisher extension; publisher-to-hub notification is
not standardized by WebSub and is not included in the claims above.
