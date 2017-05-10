This file is a template implementation report for WebSub subscribers. Copy this file to a new .md file and change the name to `PUBLISHER-project-name.md`, your project name (lowercase with hyphens between words). Fill out the information based on the details of your implementation. It's okay to not check all the boxes, we are more interested in knowing how much of the spec is implemented than getting everyone to tick every box. When you are finished, submit a pull request or link to your file in a [new issue](https://github.com/w3c/websub/issues).

For items that have a number next to the checkbox, the number corresponds with the test number on websub.rocks. You can use that tool to check whether you support the feature properly. To mark a statement as true, add an x between the brackets, e.g. [x]. If the statement does not apply to your implementation, use [na] and add a sentence explaining why it does not apply.

Delete the section above when filling out your copy of this file.

# Implementation Name (Replace this header)

Implementation Home Page URL: 

Source code repo URL(s) (optional):
* [ ] 100% open source implementation

Programming Language(s): 

Developer(s): [Name](https://you.example.com)

Answers are:
* [ ] Confirmed via websub.rocks (for applicable results)
* [ ] All results are self-reported

## Discovery

* The publisher produces URLs with the following content types:
  * [ ] HTML
  * [ ] Atom
  * [ ] RSS
  * [ ] JSON
  * Other ________
* [ ] The publisher advertises the hub and self URLs in HTTP headers
* The publisher advertises the hub and self URLs in the body of the document for the following content types:
  * [ ] HTML in <link> tags in the HTML <head>
  * [ ] HTML in <link> tags in the body (currently not allowed, but the restriction of placing the <link> tags in the <head> is *at risk* so if an implementation requires advertising the URLs in the body this limitation may be dropped)
  * [ ] Atom in <link> elements
  * [ ] RSS in <atom:link> elements
* [ ] The publisher advertises the hub URL using the `.host-meta` well-known URI (currently *at risk*)

## Distribution

* [ ] The publisher notifies the hub when a topic has been updated. (This is required, although the implementation details are not specified, in order to allow flexibility in how hubs are implemented. e.g. a hub integrated with the publishing software does not need a standardized notification mechanism.)

If your publisher uses an external hub, please describe how the publisher notifies the hub of new content:

* [ ] The publisher sends a POST request to the hub with `hub.mode=publish&hub.topic=_______`
* [ ] Other: ______________________
