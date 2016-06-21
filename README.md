# ng-sch-form-p1
Using Angular Schema Form and basing some angular forms off of the JSON schema.

# Things to brainstorm
How we'll do these things:
* Build a front-end for an evolving API which is hopefully self-documenting enough that we can build a flexible UI around it.
* Adding a layer of indirection in which the "Internal API" is self-describing and wraps one or more external APIs

# Reference

The items listed below are not comprehensive, but offer a taste of how many different ways people are attempting to solve the same problem, which is essentially "How do I effectively document this API, and how to I enable my clients to evolve with it?" (or something to this effect)

Good stuff to read:

* https://github.com/json-schema-form/angular-schema-form - Does all the hard work
 for this dynamic UI demo.
   * Jsonary might also be worth looking at? [Jsonary Github](https://github.com/jsonary-js/jsonary)
* https://spacetelescope.github.io/understanding-json-schema/index.html - Good docs on JSON schema
* [http://json-schema.org](http://json-schema.org) - Very basic JSON schema info
* The many options for specc-ing out your API:
  * [RAML](http://raml.org/)
  * [Swagger](http://swagger.io/)
  * [OData](http://www.odata.org/)
  * [Siren](https://github.com/kevinswiber/siren)
  * [JSON Home](https://github.com/otto-de/jsonhome)
* HATEOAS
  * I list HATEOAS separately since it is more of a "pattern" than a spec.
  * Paypal's HATEOAS docs: https://developer.paypal.com/docs/integration/direct/paypal-rest-payment-hateoas-links/

In practice, most of the API specs differ little from "classic" web services (and RPC).
In their defense, there are some notable advantages in leveraging the HTTP spec (and thus making APIs "RESTful"), so it is arguably "better".

However, hypermedia (and HATEOAS, for example) do represent a significant shift in how evolvable clients can be designed.
Definitely worth playing with to explore its potential.