# Readable numbers
A lesser known typescript feature is that you can include `_` in numbers. For example, `const tenSeconds: number = 10_000`. The extra underscore is removed when compiled to javascript.

Large numbers such as 1,000,000 can be written as `1_000_000`.