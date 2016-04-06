trimLeft and trimRight for ECMAScript
-------------------------------------

ES5 standardized `String.prototype.trim`. All major engines have also
implemented corresponding `String.prototype.trimLeft` and `String.prototype.trimRight` functions - without any standard specification.

Since these are defacto standard across engines, I propose that these are standardized as is.

## Bidi and Right-to-Left Strings

In [this discussion](https://esdiscuss.org/topic/string-prototype-trimright-trimleft) it was noted that the words `left` and `right` doesn't make sense for bidirectional and right-to-left languages. A more appropriate name for these functions would be `trimStart` and `trimEnd` which corresponds to the existing `startsWith` and `endsWith`.

Unfortunately, all engines already implement them and removing them would likely break the web.

## [Spec Text](Spec.md)

See [this extension](Spec.md) to the spec.

## [Status of this Proposal](https://github.com/tc39/ecma262)

It is my intention to propose this as a Stage 0 proposal to the next version of ECMAScript.
