# Dobrado

Implementation Home Page URL: https://dobrado.net

Source code repo URL(s) (optional): https://gitlab.com/dobrado/dobrado
* [x] 100% open source implementation

Programming Language(s): PHP

Developer(s): [Malcolm Blaney](https://unicyclic.com/mal)

Answers are:
* [x] Confirmed via websub.rocks (for applicable results)
* [x] All results are self-reported

## Subscription

* [x] 100: Supports subscriptions with `hub.mode`, `hub.topic` and `hub.callback`
* [ ] 101: Supports subscriptions with `hub.mode`, `hub.topic`, `hub.callback` and `hub.secret`
* [x] 102: Ignores unrecognized parameters in the subscription request
* [x] 103: Allows subscribers to re-request active subscriptions before they expire
* [ ] 104: Supports unsubscription requests
* [ ] 1xx: Sends a properly formatted verification request for subscribing and unsubscribing
* [x] Allows subscribers to request a specific lease duration
  * If not, then describe the default lease duration issued, or other specifics here

(1xx denotes that you can can use any of the 100-104 tests to confirm this feature)

## Distribution

* [x] 100: Sends a notification with a matching content-type of the topic URL
* [x] 100: Sends a notification with the full contents of the topic
* [ ] 101: Sends a notification with a valid signature
  * Please select the signature method(s) that the hub uses to sign requests
  * [ ] sha1
  * [ ] sha256
  * [ ] sha384
  * [ ] sha512
* [ ] Sends only a diff of the topic URL for Atom or RSS feeds

