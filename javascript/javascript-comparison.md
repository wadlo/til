# Javascript Comparison

## Loose comparison (==)
Similar data can sometimes be stored in different formats. For example `'5'` and `5`. Loose comparison attempts to ignore type and compare only values. There are, however edge cases that may behave differently than you'd expect.


`5 == '5'` -> `true` Strings compared to numbers will cast the string to a number

`'' == 0` -> `true` The empty string can cast to 0

`'' == undefined` -> `false` Strings and numbers cannot be cast to undefined or null

`undefined == null` -> `true`Undefined and null, however are considered loosely equal

`a = {c: 1}; b = {c: 1}; a == b` -> `false` Objects are an interesting case. Since they are not primitive, they must be the same reference to be equal. Loose comparison will be false unless it is compared with the exact same object.

`NaN == NaN` -> `false` NaN is a special edge case and is not equal to itself.

`a = NaN; a == a` -> `false` Note: Unlike with objects, `NaN` is a primitive type, not a reference. This is the same as testing `NaN == NaN`.

`0 == -0` -> `true` Comparing things that are the same type behaves the same as strict comparison

`Infinity == -Infinity` -> `false`

`'abc' == 'ab'` -> `false`

## Strict comparison (===)
`'' === 0` -> `false` If both types are primitive, they must be the same value and type.

`undefined === null` -> `false` This includes undefined and null

`0 === -0` -> `true` Numbers that are equal, but represented in different ways are strictly equal

`5 === 5.0` -> `true` These are technically the same number
