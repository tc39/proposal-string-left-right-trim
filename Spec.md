 # String.prototype.trim ( )

The following steps are taken:

  1. Let _S_ be *this* value.
  1. Return ? TrimString(_S_, `"start+end"`).

*Note:* The **trim** function is intentionally generic; it does not require that its this value be a String object. Therefore, it can be transferred to other kinds of objects for use as a method.

# String.prototype.trimStart ( )

The following steps are taken:

  1. Let _S_ be *this* value.
  1. Return ? TrimString(_S_, `"start"`).

*Note:* The **trimStart** function is intentionally generic; it does not require that its this value be a String object. Therefore, it can be transferred to other kinds of objects for use as a method

# String.prototype.trimEnd ( )

The following steps are taken:

  1. Let _S_ be *this* value.
  1. Return ? TrimString(_S_, `"end"`).

*Note:* The **trimEnd** function is intentionally generic; it does not require that its this value be a String object. Therefore, it can be transferred to other kinds of objects for use as a method

# Runtime Semantics: TrimString ( string, where )

The abstract operation TrimString is called with arguments _string_ and _where_, and interprets the String value _string_  as a sequence of UTF-16 encoded code points, as described in **6.1.4**. It performs the following steps:

  1. Let _str_ be ? RequireObjectCoercible(_string_).
  1. Let _S_ be ? ToString(_str_).
  1. If _where_ is `"start"`, let _T_ be a String value that is a copy of _S_ with leading white space removed.
  1. Else if _where_ is `"end"`, let _T_ be a String value that is a copy of _S_ with trailing white space removed.
  1. Else,
    1. Assert: _where_ is `"start+end"`.
    1. Let _T_ be a String value that is a copy of _S_ with both leading and trailing white space removed.
  1. Return _T_.

The definition of white space is the union of *WhiteSpace* and *LineTerminator*. When determining whether a Unicode code point is in Unicode general category &ldquo;Zs&rdquo;, code unit sequences are interpreted as UTF-16 encoded code point sequences as specified in **6.1.4**.

# String.prototype.trimLeft ( )

*Note:* The property **trimStart** is preferred. The **trimLeft** property is provided principally for compatibility with old code. It is recommended that the **trimStart** property be used in new ECMAScript code.

The function object that is the initial value of **String.prototype.trimLeft** is the same function object that is the initial value of **String.prototype.trimStart**.

# String.prototype.trimRight ( )

*Note:* The property **trimEnd** is preferred. The **trimRight** property is provided principally for compatibility with old code. It is recommended that the **trimEnd** property be used in new ECMAScript code.

The function object that is the initial value of **String.prototype.trimRight** is the same function object that is the initial value of **String.prototype.trimRight**.
