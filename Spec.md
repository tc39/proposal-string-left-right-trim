## String Trim Functions

**String.prototype.trim ( )**

Return result of `StringTrim` abstract operation passing **this** value as `thisArg`, and `TrimBoth` as the `type`.

**String.prototype.trimRight ( )**

Return result of `StringTrim` abstract operation passing **this** value as `thisArg`, and `TrimRight` as the `type`.

**String.prototype.trimLeft ( )**

Return result of `StringTrim` abstract operation passing **this** value as `thisArg`, and `TrimLeft` as the `type`.

NOTE: The **trim**, **trimLeft**, and **trimRight** functions are intentionally generic; they do not require that their **this** value be a String object. Therefore, they can be transferred to other kinds of objects for use as a method.

## Helper Abstract Operations

**StringTrim(thisArg, type) abstract operation**

This function interprets a string value as a sequence of UTF-16 encoded code points, as described in <...>.

The following steps are taken:

1. Let _O_ be `RequireObjectCoercible`(_thisArg_).
2. Let _S_ be ToString(_O_).
3. `ReturnIfAbrupt`(S).
4. Let _T_ be a String value that is a copy of _S_ with:
  * if _type_ is `TrimBoth`, then with both leading and trailing white space removed
  * else if _type_ is `TrimRight`, then with trailing white space removed
  * else if _type_ is `TrimgLeft`, then both leading white space removed
  * NOTE: The definition of white space is the union of _WhiteSpace_ and _LineTerminator._ When determining whether a Unicode code point is in Unicode general category _"Zs"_, code unit sequences are interpreted as UTF-16 encoded code point sequences as specified in <...>.
5. Return _T_.
