# Ballerina

Implementation Home Page URL: [ballerina/websub](https://central.ballerina.io/ballerina/websubhub/latest) 

Source code repo URL(s) (optional): https://github.com/ballerina-lang/ballerina
* [x] 100% open source implementation

Programming Language(s): Ballerina 

Developer(s): [Ballerina](https://ballerina.io/)

Answers are:
* [x] Confirmed via websub.rocks (for applicable results)
* [ ] All results are self-reported

## Subscription

* [x] 100: Supports subscriptions with `hub.mode`, `hub.topic` and `hub.callback`  
* [x] 101: Supports subscriptions with `hub.mode`, `hub.topic`, `hub.callback` and `hub.secret`
  * Self-reported with JSON content  
* [x] 102: Ignores unrecognized parameters in the subscription request
* [x] 103: Allows subscribers to re-request active subscriptions before they expire
* [x] 104: Supports unsubscription requests
* [x] 1xx: Sends a properly formatted verification request for subscribing and unsubscribing
* [x] Allows subscribers to request a specific lease duration
  * If not, then describe the default lease duration issued, or other specifics here

(1xx denotes that you can can use any of the 100-104 tests to confirm this feature)

## Distribution

* [x] 100: Sends a notification with a matching content-type of the topic URL
  * publisher defines content to deliver  
* [x] 100: Sends a notification with the full contents of the topic
* [x] 101: Sends a notification with a valid signature
  * Please select the signature method(s) that the hub uses to sign requests
  * [x] sha1
  * [x] sha256
  * [x] sha384
  * [x] sha512
* [ ] Sends only a diff of the topic URL for Atom or RSS feeds

