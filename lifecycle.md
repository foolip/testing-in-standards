# Testing in standards: from idea to full interop

*This is an opinion on how to integrate testing into the standards lifecycle. It is well aligned with the [WHATWG working mode](https://whatwg.org/working-mode) and [W3C testing how-to](https://github.com/w3c/testing-how-to/) but has no official status.*

## Summary

The primary purpose of standards is to achieve interoperable implementations, and the desired outcome is full interoperability that web developers can depend on. By writing and sharing tests as soon as implementation begins and making testing an integrated part of the standards process, we can reduce the overall cost/time of evolving the web platform and achieve good interop by default.

(See "[Finding a path to interop](https://docs.google.com/document/d/1LSuLWJDP02rlC9bOlidL6DzBV5kSkV5bW5Pled8HGC8/edit?usp=sharing)" for definitions of *interoperability* and *full interoperability*.)

## Lifecycle

### Idea

In the earliest stages, only an [explainer](https://docs.google.com/document/d/1cJs7GkdQolqOHns9k6v1UjCUb_LqTFVjZM-kc3TbNGI/edit?usp=sharing) will exist, there will be no standard, no tests, and no implementation.

### First implementation

If the idea gets traction, at some point a first implementation will begin. This could be before or after the standard has begun to take shape, but for any non-trivial idea will be well before the standard is fully formed.

All tests for web-exposed behavior that are written for the first implementation should be shared. They will fall into one of two categories:
 1. The standard already covers this behavior. Write regular tests. 
 2. The standard doesn't, or no standard exists yet. Then, write [tentative tests](http://web-platform-tests.org/writing-tests/file-names.html#test-features). Make it clear why the test is tentative, for example with a link to an open spec issue.

Tentative tests should be revisited and converted to regular tests as the standard catches up. Because they were originally not reviewed against any spec text, converted tests must be reviewed as if they were new, not as a simple renaming.

By the time the first implementation ships there should ideally be no tentative tests.

### Testing policy

When the first implementation ships, the standard and tests ought to be in good shape, so asking "What do implementations do?" and "What do the tests reveal?" for spec changes (see [WHATWG working mode](https://whatwg.org/working-mode)) becomes relevant. Around this time it would make sense to adopt a [policy for testing normative spec changes](policy.md).

### Second implementation

A second implementer will almost certainly discover spec bugs, test bugs and missing test coverage. This will result in new failing tests for the first implementer, which should be very welcome. (Without shared tests, interop problems could otherwise go unnoticed until much later.)

### Mature standard

Following implementers will find a standard and test suite that are in increasingly good shape, and the existing test suite should lower the time/cost to implement.

For a mature standard, the whole process can repeat for proposed changes. New ideas start as issues, tests are modified or added, and implementer experience helps shape the spec and tests into their final form.

### Full interop

As the standard, test suite and implementations co-evolve, an increasing number of tests will pass everywhere. For those tests, however trivial, full interop has been achieved. Once achieved, tooling should make it impossible to accidentally depart from full interop. Web developers can depend on the feature to work the same way in any browser.

## Examples
 * HTML: the `messageerror` event had [spec text](https://github.com/whatwg/html/pull/2530) and [tests](https://github.com/w3c/web-platform-tests/pull/5567) written side-by-side and merged together, before any implementation.
 * Fetch: aborting [spec change](https://github.com/whatwg/fetch/pull/523) and [tests](https://github.com/w3c/web-platform-tests/pull/6484) also written together, and test bug fixed during [implementation](https://bugzilla.mozilla.org/show_bug.cgi?id=1378342).
 * Trusted Types: [explainer](https://github.com/mikewest/trusted-types/blob/master/README.md) and [tentative tests](https://github.com/w3c/web-platform-tests/tree/cbc2da38b90e0870ac50a205d2fc2773de41bd5d/trusted-types) written before spec text.

Note: The order of spec text, tests and implementation isn't always the same, and it's not clear that there's a single best order. Any working mode that feels productive and results in quality all around should be embraced.

## Risks

Risks of tentative tests in web-platform-tests:
 * If treated like regular tests, they would influence incentives. (See wpt.fyi issues [#83](https://github.com/w3c/wptdashboard/issues/83) and [#99](https://github.com/w3c/wptdashboard/issues/99).)
 * When converting tentative tests to regular tests, it is tempting to do very light review.
 * Without a triage process, they might be left for a very long time. (TODO)

Risks of engine-specific tests:
 * Shared tests wouldn't be the initial default, making it more tempting to use vendor-specific testing APIs.
 * Upstreaming a large number of engine-specific tests is some amount of work, and risks being delayed.
 * If a second implementer becomes interested early, they might be blocked on the first implementer sharing their tests.

It's not an open-and-shut case, but sharing tests as early as possibly seems best.

## Resources
 * The web-platform-tests documentation on [writing](http://web-platform-tests.org/writing-tests/) and [reviewing](http://web-platform-tests.org/reviewing-tests/) tests
 * The [web-platform-tests dashboard](https://wpt.fyi/) (wpt.fyi)
 * The [web-platform-tests PR results](https://pulls.web-platform-tests.org) (posts comments to GitHub PRs)
 * Chromium's documentation on [web-platform-tests](https://chromium.googlesource.com/chromium/src/+/master/docs/testing/web_platform_tests.md), [writing layout tests](https://chromium.googlesource.com/chromium/src/+/master/docs/testing/writing_layout_tests.md) and the [layout tests tips](https://chromium.googlesource.com/chromium/src/+/master/docs/testing/layout_tests_tips.md)
