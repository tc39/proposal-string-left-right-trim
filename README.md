# String.prototype.trimStart / String.prototype.trimEnd

ECMAScript proposal, specs, tests, and reference implementation for String.prototype.trimStart/trimEnd (plus **trimLeft/trimRight**).

**Stage 4**

This proposal is complete and already merged into [ECMA262 specification](https://tc39.es/ecma262/). See the specification text here.

## Rationale
ES5 standardized `String.prototype.trim`. All major engines have also implemented corresponding `trimLeft` and `trimRight` functions - without any standard specification.
For consistency with `padStart`/`padEnd` we propose `trimStart` and `trimEnd` and `trimLeft`/`trimRight` as aliases required for web compatibility.

## Specification
You can view the spec in [ecmarkup](spec.emu) or rendered as [HTML](https://tc39.github.io/proposal-string-left-right-trim/).

## Naming / Aliasing
For consistency with `padStart`/`padEnd` the standard functions will be `trimStart` and `trimEnd`, however for web compatilibity `trimLeft` will alias `trimStart` and `trimRight` will alias `trimEnd`. This means `String.prototype.trimRight.name` will change from `"trimRight"` to `"trimEnd"` in most engines. The spec author does not expect this to cause any breakage.

## Test262 Coverage

[PR open](https://github.com/tc39/test262/pull/1246)

## Status of This Proposal

This initial proposal was drafted by [@sebmarkbage](https://github.com/sebmarkbage) and the updated spec was drafted by [@evilpie](https://github.com/evilpie/) with input from [@ljharb](https://github.com/ljharb).

This proposal is currently at [stage 4](https://github.com/tc39/ecma262) of the [process](https://tc39.github.io/process-document/).

Designated TC39 reviewers: Jordan Harband + Daniel Ehrenberg

## Implementations

- [V8](https://bugs.chromium.org/p/v8/issues/detail?id=6530), in Chrome 66+
- [SpiderMonkey](https://bugzilla.mozilla.org/show_bug.cgi?id=1434007#c12), in Firefox 61+
- [JSC](https://bugs.webkit.org/show_bug.cgi?id=26590), in Safari 12+
- [ChakraCore](https://github.com/Microsoft/ChakraCore/pull/5693)
