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

## Discovery

* The publisher produces URLs with the following content types:
  * [x] HTML
  * [ ] Atom
  * [ ] RSS
  * [ ] JSON
  * [x] Other: It's a library. A user can add it around a Flask route of any
        content type. That said, there are special helper functions for html
        <link> tags. Link headers are always set automatically.
* [x] The publisher advertises the hub and self URLs in HTTP headers
* The publisher advertises the hub and self URLs in the body of the document for the following content types:
  * [na] HTML in <link> tags in the HTML <head>
  * [na] HTML in <link> tags in the body (currently not allowed, but the restriction of placing the <link> tags in the <head> is *at risk* so if an implementation requires advertising the URLs in the body this limitation may be dropped)
  * [na] Atom in <link> elements
  * [na] RSS in <atom:link> elements
  * There is a helper for creating a link tag, the user decides where to use
    it in their Flask route.
* [ ] The publisher advertises the hub URL using the `.host-meta` well-known URI (currently *at risk*)

## Distribution

* [na] The publisher notifies the hub when a topic has been updated. (This is required, although the implementation details are not specified, in order to allow flexibility in how hubs are implemented. e.g. a hub integrated with the publishing software does not need a standardized notification mechanism.)
  * Up to the user. A library does not know when the underlying data store changes.
If your publisher uses an external hub, please describe how the publisher notifies the hub of new content:

* [ ] The publisher sends a POST request to the hub with `hub.mode=publish&hub.topic=_______`
* [ ] Other: ______________________
* Publishing to an integrated hub is a single function call. To an external hub
  is up to the user completely.
