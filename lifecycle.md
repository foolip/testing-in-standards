# Testing in standards: from idea to interop

*This is an opinion on how to integrate testing into the standards lifecycle. It is well aligned with the [WHATWG working mode](https://whatwg.org/working-mode) and [W3C testing how-to](https://github.com/w3c/testing-how-to/) but has no official status.*

## Summary

The primary purpose of standards is to achieve interoperable implementations, and the desired outcome is full interoperability that web developers can depend on. By writing and sharing tests as soon as implementation begins and making testing an integrated part of the standards process, the time from idea to real-world interop should be shortened.

## Definitions
 * An **API** is any behavior that is web exposed, typically being observable directly by scripts, but also by changing what is rendered, what audio is played, how assistive technology behaves, etc..
 * **Interoperability** is when an API has the same web exposed behavior in multiple browser engines, and **full interoperability** is when it behaves the same in all engines that are in wide use, currently Blink, EdgeHTML, Gecko and WebKit.
 * **Conformance** is when an implementation matches the normative requirements of the standard.
 * **Compatibility** is when an implementation actually works with web pages "in the wild."

(From "[Finding a path to interop](https://docs.google.com/document/d/1LSuLWJDP02rlC9bOlidL6DzBV5kSkV5bW5Pled8HGC8/edit?usp=sharing)")

## Lifecycle

### Idea

In the earliest stages, only an explainer ([example](https://github.com/w3c/ServiceWorker/blob/master/explainer.md)) will exist, there will be no spec and no implementation. At this point, writing tests will generally not be a good use of time.

If the idea has merit, at some point a first implementation will begin to take shape. Whether this happens before or after the spec TODO

### First implementation

Write tentative tests if there is no spec, otherwise plain tests. As the spec is fleshed out, convert tentative tests to normal tests. Super extra special care needed to vet tests at this point. [Tentative tests should be excluded from wpt.fyi](https://github.com/w3c/wptdashboard/issues/99).

Time to adopt a [policy](policy.md) around testing?

### Second implementation

Second implementer still needs to be skeptical of the tests and their coverage. Write more, fix the spec!

### Full interoperability

For a mature standard, the [WHATWG working mode](https://whatwg.org/working-mode) works well.

## What about?

### Writing tests as soon as there is a spec?

It's hard to write very deep tests without an implementation.

### Tying testing policy to Candidate Recommendations (CR)?

Implementation may have begun much earlier.

### Coverage?

There's a long history of trying to figure out how to asses how well a test suite covers its spec. Tooling around this could still be worth investigating. However, by having shared tests be the only tests, we lean on the code review practices of all engines to notice when what is being implemented is insufficiently tested.
