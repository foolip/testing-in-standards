# Testing policy

The history and purpose of testing normative changes is explained in the blog post "[improving interoperability](https://blog.whatwg.org/improving-interoperability)." Through outreach efforts in [2017 Q2, Q3](https://docs.google.com/document/d/1aRpnNQ7Zz_-N9ngdcjQXNjlE1NblppN7lCQwGdxRLlc/edit?usp=sharing) and [Q4](https://docs.google.com/document/d/1GZquS8Jra47E5hIMH2ObOb_7oQFgk8f9MptUAjF0LFI/edit?usp=sharing) – and momentum – the hope is that soon testing will be an integral part of virtually all web standards work.

See "[from idea to full interop](lifecycle.md)" for how this might fit into the standards lifecycle. The "[improving interop with web-platform-tests](https://webengineshackfest.org/#portfolio)" talk also covers some of the same ground.

## Progress
 * WHATWG [contributor](https://github.com/whatwg/meta/blob/master/CONTRIBUTING.md#tests) and [maintainer](https://github.com/whatwg/meta/blob/master/TEAM.md) guidelines ([issue](https://github.com/whatwg/html/issues/1849)) (16 specs)
 * [Service Workers](https://github.com/w3c/ServiceWorker/blob/master/CONTRIBUTING.md) ([PR](https://github.com/w3c/ServiceWorker/pull/1131))
 * [Web Performance WG](https://github.com/w3c/web-performance/blob/gh-pages/CONTRIBUTING.md#test-driven) ([PR](https://github.com/w3c/web-performance/pull/17)) (12 specs)
 * [IndexedDB](https://github.com/w3c/IndexedDB/blob/master/CONTRIBUTING.md#tests) ([PR](https://github.com/w3c/IndexedDB/pull/200))
 * [Pointer Lock](https://github.com/w3c/pointerlock/blob/gh-pages/CONTRIBUTING.md#tests) ([PR](https://github.com/w3c/pointerlock/pull/20))
 * [Payment Request](https://github.com/w3c/payment-request/blob/gh-pages/test-plan.md) ([commit](https://github.com/w3c/payment-request/commit/139f8b3e2779aadb0a5e4f88c77600dc40405a7a#diff-6684f7304df8a395938c0636514a7461))
 * [Web Animations](https://github.com/w3c/web-animations/blob/master/CONTRIBUTING.md#tests) ([PR](https://github.com/w3c/web-animations/pull/194))
 * [WebVTT](https://github.com/w3c/webvtt/blob/gh-pages/CONTRIBUTING.md#tests) ([PR](https://github.com/w3c/webvtt/pull/357))
 * [FX Task Force](https://github.com/w3c/fxtf-drafts/blob/master/CONTRIBUTING.md#tests) ([PR](https://github.com/w3c/fxtf-drafts/pull/215)), covering 6 maintained specs:
   * [Compositing and Blending](https://drafts.fxtf.org/compositing/)
   * [CSS Masking](https://drafts.fxtf.org/css-masking/)
   * [CSS Fill and Stroke](https://drafts.fxtf.org/fill-stroke/)
   * [Filter Effects](https://drafts.fxtf.org/filter-effects/)
   * [Geometry Interfaces](https://drafts.fxtf.org/geometry/)
   * [Motion Path](https://drafts.fxtf.org/motion/)
 * [CSSWG](https://github.com/w3c/csswg-drafts/blob/master/CONTRIBUTING.md#tests) ([minutes](https://www.w3.org/2017/08/03-css-minutes.html#item06), [issue](https://github.com/w3c/csswg-drafts/issues/1755), [PR](https://github.com/w3c/csswg-drafts/pull/1767)) (32 specs in [CR or later](https://www.w3.org/Style/CSS/current-work) + CSSOM + CSSOM View)
 * [Intersection Observer](https://github.com/w3c/IntersectionObserver/blob/master/CONTRIBUTING.md#tests) ([commit](https://github.com/w3c/IntersectionObserver/commit/1b81b995fd9a1d208b452f20327b5a5921bffb41))
 * [SVGWG](https://github.com/w3c/svgwg/blob/master/CONTRIBUTING.md#tests) ([commit](https://github.com/w3c/svgwg/commit/18eb74f259296423a25538dacb6519b812ad179f), [charter](https://www.w3.org/2017/04/svg-2017.html#deliverables), [background](https://github.com/w3c/testing-how-to/pull/4)) (8 specs)
 * [Content Security Policy](https://github.com/w3c/webappsec-csp/blob/master/CONTRIBUTING.md#tests) ([PR](https://github.com/w3c/webappsec-csp/pull/230))
 * Device APIs Working Group:
    * [[DRAFT] Devices and Sensors Working Group Charter](https://w3c.github.io/dap-charter/DeviceAPICharter.html#deliverables) ([PR](https://github.com/w3c/dap-charter/pull/51))
    * [Ambient Light](https://github.com/w3c/ambient-light/blob/gh-pages/CONTRIBUTING.md#tests) ([PR](https://github.com/w3c/ambient-light/pull/47))
   * [Accelerometer](https://github.com/w3c/accelerometer/blob/gh-pages/CONTRIBUTING.md#tests) ([PR](https://github.com/w3c/accelerometer/pull/29))
   * [Battery Status API](https://github.com/w3c/battery/blob/gh-pages/CONTRIBUTING.md#tests) ([PR](https://github.com/w3c/battery/pull/14))
   * [Generic Sensor API](https://github.com/w3c/sensors/blob/master/CONTRIBUTING.md#tests) ([PR](https://github.com/w3c/sensors/pull/316))
   * [Gyroscope](https://github.com/w3c/gyroscope/blob/gh-pages/CONTRIBUTING.md#tests) ([PR](https://github.com/w3c/gyroscope/pull/26))
   * [HTML Media Capture](https://github.com/w3c/html-media-capture/blob/gh-pages/CONTRIBUTING.md#tests) ([PR](https://github.com/w3c/html-media-capture/pull/18))
   * [Magnetometer](https://github.com/w3c/magnetometer/blob/gh-pages/CONTRIBUTING.md#tests) ([PR](https://github.com/w3c/magnetometer/pull/38))
   * [Orientation Sensor](https://github.com/w3c/orientation-sensor/blob/gh-pages/CONTRIBUTING.md#tests) ([PR](https://github.com/w3c/orientation-sensor/pull/52))
 * [Clipboard API and Events](https://github.com/w3c/clipboard-apis/blob/master/CONTRIBUTING.md#tests) ([PR](https://github.com/w3c/clipboard-apis/pull/56))
 * [File API](https://github.com/w3c/FileAPI/blob/gh-pages/CONTRIBUTING.md#tests) ([PR](https://github.com/w3c/FileAPI/pull/85))
 * [Static Range](https://github.com/w3c/staticrange/blob/gh-pages/CONTRIBUTING.md#tests) ([PR](https://github.com/w3c/staticrange/pull/11))
 * [UI Events](https://github.com/w3c/uievents/blob/gh-pages/CONTRIBUTING.md#tests) ([PR](https://github.com/w3c/uievents/pull/163))
 * [File and Directory Entries](https://github.com/WICG/entries-api/blob/gh-pages/CONTRIBUTING.md#tests) ([PR](https://github.com/WICG/entries-api/pull/22))
 * [Resize Observer](https://github.com/WICG/ResizeObserver/blob/master/CONTRIBUTING.md#tests) ([PR](https://github.com/WICG/ResizeObserver/pull/44))
 * [Web Audio API](https://github.com/WebAudio/web-audio-api/blob/gh-pages/README.md#tests) ([PR](https://github.com/WebAudio/web-audio-api/pull/1423))
 * [Keyboard Lock](https://github.com/w3c/keyboard-lock/blob/gh-pages/README.md#tests) ([PR](https://github.com/w3c/keyboard-lock/pull/36))
 * [WebUSB](https://github.com/WICG/webusb/blob/master/CONTRIBUTING.md#tests) ([PR](https://github.com/WICG/webusb/pull/109))
 * [Feature Policy](https://github.com/WICG/feature-policy/blob/gh-pages/CONTRIBUTING.md#tests) ([PR](https://github.com/WICG/feature-policy/pull/91)) (wording tweak, copy from this one)
 * [Vibration](https://github.com/w3c/vibration/blob/gh-pages/CONTRIBUTING.md#tests) ([PR](https://github.com/w3c/vibration/pull/20))
 * [Touch Events](https://github.com/w3c/touch-events/blob/gh-pages/README.md#tests) ([PR](https://github.com/w3c/touch-events/pull/90))
 * [Gamepad API](https://github.com/w3c/gamepad/blob/gh-pages/CONTRIBUTING.md#tests) ([PR](https://github.com/w3c/gamepad/pull/64))
 * [WebVR](https://github.com/w3c/webvr/blob/master/README.md#tests) ([PR](https://github.com/w3c/webvr/pull/295))
 * [DOM Parsing and Serialization](https://github.com/w3c/DOM-Parsing/blob/gh-pages/CONTRIBUTING.md#tests) ([PR](https://github.com/w3c/DOM-Parsing/pull/32))

This is ~90 specs.

# Ongoing work

In https://foolip.github.io/day-to-day/ there are ~200 specs, so ~110 remain.

See "[a policy for web-platform-tests coverage is adopted for 40 more specs](https://docs.google.com/document/d/1GZquS8Jra47E5hIMH2ObOb_7oQFgk8f9MptUAjF0LFI/edit#heading=h.3jtyy5sjt1rp)" in Ecosystem Infra 2017 Q4 OKRs.
