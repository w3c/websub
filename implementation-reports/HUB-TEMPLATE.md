This file is a template implementation report for WebSub subscribers. Copy this file to a new .md file and change the name to your project name (lowercase with hyphens between words). Fill out the information based on the details of your implementation. It's okay to not check all the boxes, we are more interested in knowing how much of the spec is implemented than getting everyone to tick every box. When you are finished, submit a pull request or link to your file in a [new issue](https://github.com/w3c/websub/issues).

For items that have a number next to the checkbox, the number corresponds with the test number on websub.rocks. You can use that tool to check whether you support the feature properly. To mark a statement as true, add an x between the brackets, e.g. [x]. If the statement does not apply to your implementation, use [na] and add a sentence explaining why it does not apply.

# Implementation Name (Replace this header)

Implementation Home Page URL: 

Source code repo URL(s) (optional):
* [ ] 100% open source implementation

Programming Language(s): 

Developer(s): [Name](https://you.example.com)

Answers are:
* [ ] Confirmed via websub.rocks (for applicable results)
* [ ] All results are self-reported

## Subscription

* [ ] 100: Supports subscriptions with `hub.mode`, `hub.topic` and `hub.callback`
* [ ] 101: Supports subscriptions with `hub.mode`, `hub.topic`, `hub.callback` and `hub.secret`
* [ ] 102: Ignores unrecognized parameters in the subscription request
* [ ] 103: Allows subscribers to re-request active subscriptions before they expire
* [ ] 104: Supports unsubscription requests
* [ ] Allows subscribers to request a specific lease duration
 * If not, then describe the default lease duration issued, or other specifics here

## Distribution

* [ ] 100: Sends a notification with a matching content-type of the topic URL
* [ ] 100: Sends a notification with the full contents of the topic
* [ ] 101: Sends a notification with a valid signature
 * Please select the signature method(s) that the hub uses to sign requests
 * [ ] sha1
 * [ ] sha256
 * [ ] sha384
 * [ ] sha512
* [ ] Sends only a diff of the topic URL for Atom or RSS feeds

