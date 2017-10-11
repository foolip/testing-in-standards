# Testing in standards: from idea to full interop

*This is an opinion on how to integrate testing into the standards lifecycle. It is well aligned with the [WHATWG working mode](https://whatwg.org/working-mode) and [W3C testing how-to](https://github.com/w3c/testing-how-to/) but has no official status.*

## Summary

The primary purpose of standards is to achieve interoperable implementations, and the desired outcome is full interoperability that web developers can depend on. By writing and sharing tests as soon as implementation begins and making testing an integrated part of the standards process, we can reduce the overall cost/time of evolving the web platform and achieve good interoperability by default.

(See "[Finding a path to interop](https://docs.google.com/document/d/1LSuLWJDP02rlC9bOlidL6DzBV5kSkV5bW5Pled8HGC8/edit?usp=sharing)" for definitions of *interoperability* and *full interoperability*.)

## Lifecycle

### Idea

In the earliest stages, only an explainer ([example](https://github.com/w3c/ServiceWorker/blob/master/explainer.md)) will exist, there will be no standard and no implementation. At this point, writing tests will probably not be a good use of time.

### First implementation

If the idea gets traction, at some point a first implementation will begin. This could be before or after the standard has begun to take shape, but for any non-trivial idea will be well before the standard is fully formed.

All tests for web-exposed behavior that are written for the first implementation should be shared. They will fall into one of two categories:
 1. The standard already covers this behavior. Write regular tests. 
 2. The standard doesn't, or no standard exists yet. Then, write [tentative tests](http://web-platform-tests.org/writing-tests/file-names.html#test-features). Make it clear why the test is tentative, for example with a link to an open spec issue.

Tentative tests should be revisited and converted to regular tests as the standard catches up. Because they were originally not reviewed against any spec text, converted tests must be reviewed as if they were new, not as a simple renaming.

By the time the first implementation ships there should ideally be no tentative tests.

### Testing policy

When the first implementation ships, the standard and tests ought to be in good shape, so asking "What do implementations do?" and "What do the tests reveal?" for spec changes (see [WHATWG working mode](https://whatwg.org/working-mode)) becomes relevant. Around this time it would make sense to adopt a [policy for testing normative spec changes](policy.md).

The [web-platform-tests dashboard](https://wpt.fyi) or similar can be used to determine the status of tests.

### Second implementation and beyond

A second implementer will almost certainly discover spec bugs, test bugs and missing test coverage. This will result in new failing tests for the first implementer, which is a very good outcome. (Without shared tests, interop problems could otherwise go unnoticed until much later.)

Following implementers will find a standard and test suite that is in increasingly good shape, which should reduce the total time required to implement and ship.

### Full interop

As the standard, test suite and implementations co-evolve, an increasing number of tests will pass everywhere. For those tests, however trivial, full interop has been achieved. Once achieved, tooling like [web-platform-tests PR status](https://pulls.web-platform-tests.org) and the [web-platform-tests dashboard](https://wpt.fyi) should make it impossible to accidentally depart from full interop.
