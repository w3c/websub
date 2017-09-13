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

## Subscription

* [x] 100: Supports subscriptions with `hub.mode`, `hub.topic` and `hub.callback`
* [na] 101: Supports subscriptions with `hub.mode`, `hub.topic`, `hub.callback` and `hub.secret`
  I implemented this, but I did not test it with HTTPS enabled yet, so the test
  does not actually send the secret.
* [x] 102: Ignores unrecognized parameters in the subscription request
* [x] 103: Allows subscribers to re-request active subscriptions before they expire
* [x] 104: Supports unsubscription requests
* [x] 1xx: Sends a properly formatted verification request for subscribing and unsubscribing
* [x] Allows subscribers to request a specific lease duration
  * within configurable limits, at least. If the subscriber does not specify a
    lease duration, a configurable default is used. If the library user
    specifies nothing, the defaults are:
    - min: a minute
    - default: 10 days
    - max: 31 days

## Distribution

* [x] 100: Sends a notification with a matching content-type of the topic URL
* [x] 100: Sends a notification with the full contents of the topic
* [x] 101: Sends a notification with a valid signature
  * Please select the signature method(s) that the hub uses to sign requests
  * [x] sha1
  * [x] sha256
  * [x] sha384
  * [x] sha512 (This is the default. It's configurable.)
* [na] Sends only a diff of the topic URL for Atom or RSS feeds
  No, but the library does allow you to set the body to sent yourself. So a
  user could make it return a diff.
