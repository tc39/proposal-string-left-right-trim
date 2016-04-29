# String.prototype.trimStart / String.prototype.trimEnd

ECMAScript proposal, specs, tests, and reference implementation for String.prototype.trimStart/trimEnd (plus **trimLeft/trimRight**).

This initial proposal was drafted by [@sebmarkbage](https://github.com/sebmarkbage) and the updated spec was drafted by [@evilpie](https://github.com/evilpie/) with input from [@ljharb](https://github.com/ljharb).

This proposal is currently at [stage 1](https://github.com/tc39/ecma262) of the [process](https://tc39.github.io/process-document/).

Designated TC39 reviewers: ?

## Rationale
ES5 standardized `String.prototype.trim`. All major engines have also implemented corresponding `trimLeft` and `trimRight` functions - without any standard specification.
For consinstency with `padStart`/`padRight` we propose `trimStart` and `trimEnd` and `trimLeft`/`trimRight` as aliases required for web compatibility.

## Spec
You can view the spec in [markdown format](Spec.md) or rendered as [HTML](https://sebmarkbage.github.io/ecmascript-string-left-right-trim/).

## Naming / Aliasing
For consinstency with `padStart`/`padEnd` the standard functions will be `trimStart` and `trimEnd`, however for web compatilibity `trimLeft` will alias `trimStart` and `trimRight` will alias `trimEnd`. This means `String.prototype.trimRight.name` will change from `"trimRight"` to `"trimEnd"` in most engines. The spec author does not expect this to cause any breakage.
