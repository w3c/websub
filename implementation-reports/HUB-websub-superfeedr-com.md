# http://websub.superfeedr.com/

Implementation Home Page URL: http://websub.superfeedr.com/

Developer(s): [Superfeedr](https://superfeedr.com/)

Answers are:
* [X] Confirmed via websub.rocks (for applicable results)
* [ ] All results are self-reported

## Subscription

* [X] 100: Supports subscriptions with `hub.mode`, `hub.topic` and `hub.callback`
* [X] 101: Supports subscriptions with `hub.mode`, `hub.topic`, `hub.callback` and `hub.secret`
* [X] 102: Ignores unrecognized parameters in the subscription request
* [X] 103: Allows subscribers to re-request active subscriptions before they expire
* [X] 104: Supports unsubscription requests
* [X] 1xx: Sends a properly formatted verification request for subscribing and unsubscribing
* [X] Allows subscribers to request a specific lease duration
  * If not, then describe the default lease duration issued, or other specifics here

(1xx denotes that you can can use any of the 100-104 tests to confirm this feature)

## Distribution

* [X] 100: Sends a notification with a matching content-type of the topic URL
* [X] 100: Sends a notification with the full contents of the topic
* [X] 101: Sends a notification with a valid signature
  * Please select the signature method(s) that the hub uses to sign requests
  * [X] sha1
  * [ ] sha256
  * [ ] sha384
  * [ ] sha512
* [X] Sends only a diff of the topic URL for Atom or RSS feeds

