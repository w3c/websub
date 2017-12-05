# Twtich

Implementation Home Page URL: https://dev.twitch.tv/docs/api/webhooks-guide

Source code repo URL(s) (optional):
* [ ] 100% open source implementation

Programming Language(s): Go

Developer(s): [Jordan Potter](jordanpotter@twitch.tv)

Answers are:
* [ ] Confirmed via websub.rocks (for applicable results)
* [x] All results are self-reported

## Subscription

* [x] 100: Supports subscriptions with `hub.mode`, `hub.topic` and `hub.callback`
* [x] 101: Supports subscriptions with `hub.mode`, `hub.topic`, `hub.callback` and `hub.secret`
* [x] 102: Ignores unrecognized parameters in the subscription request
* [x] 103: Allows subscribers to re-request active subscriptions before they expire
* [x] 104: Supports unsubscription requests
* [x] 1xx: Sends a properly formatted verification request for subscribing and unsubscribing
* [x] Allows subscribers to request a specific lease duration
  * If not, then describe the default lease duration issued, or other specifics here

(1xx denotes that you can can use any of the 100-104 tests to confirm this feature)

## Distribution

* [ ] 100: Sends a notification with a matching content-type of the topic URL
* [ ] 100: Sends a notification with the full contents of the topic
* [x] 101: Sends a notification with a valid signature
  * Please select the signature method(s) that the hub uses to sign requests
  * [ ] sha1
  * [x] sha256
  * [ ] sha384
  * [ ] sha512
* [ ] Sends only a diff of the topic URL for Atom or RSS feeds
