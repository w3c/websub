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

## Subscription

* [ ] 100: Supports subscriptions with `hub.mode`, `hub.topic` and `hub.callback`
* [x] 101: Supports subscriptions with `hub.mode`, `hub.topic`, `hub.callback` and `hub.secret`
* [x] 102: Ignores unrecognized parameters in the subscription request
* [x] 103: Allows subscribers to re-request active subscriptions before they expire
* [x] 104: Supports unsubscription requests
* [x] 1xx: Sends a properly formatted verification request for subscribing and unsubscribing
* [x] Allows subscribers to request a specific lease duration
  * A min/max range is enforced

## Distribution

* [x] 100: Sends a notification with a matching content-type of the topic URL
* [ ] 100: Sends a notification with the full contents of the topic
* [ ] 101: Sends a notification with a valid signature
  * Please select the signature method(s) that the hub uses to sign requests
  * [x] sha1
  * [ ] sha256
  * [ ] sha384
  * [ ] sha512
* [x] Sends only a diff of the topic URL for Atom or RSS feeds

