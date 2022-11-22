When we run `toString()` on an array, let's say `a = ["ab", "cd"]`, it returns something like `[C@6e1408`. What does that mean?
> Something like `[C@6e1408` is certainly not random gibberish - it's the same way of constructing a string from an object as any other type that doesn't override `toString()` inherits - it's a representation of the type (`[` indicating an array; `C` indicating the char primitive type) followed by the identity hash code in hex. [See the documentation](https://docs.oracle.com/javase/7/docs/api/java/lang/Object.html#toString%28%29) for `Object.toString()` for details. As it happens, arrays don't override `toString`.