## Common Lisp v. Scheme
(*nb. Yes, I'm a Schemer and yes these complaints are highly biased*)
Let's take a quick look at some Common Lisp's functions as examples, comparing them 
to their Scheme-equivalent functions, and I'll let you act the role of an impartial judge
presiding over the case **Common Lisp v. Common sense**:

| Common Lisp | Scheme     | What it does?                                       |
|:-----------:|:----------:|:----------------------------------------------------|
| `progn`     | `begin`    | The *`expr`s* are evaluated from left-to-right, with only the last *`expr`* returning a value. |
| `terpri`    | `newline`  | Prints a newline, as in a `\n`.                     |
| `princ`     | `display`  | Input, *`obj`*, is represented in a human-readable format: strings are displayed without double quotes and escapes. |
| `prin1`     | `write`    | Input, *`obj`*, is sanitized, ie. strings are put in double quotes, with escapes where neccesary, and represented in a machine-readable format. This allows the representation of *`obj`* to  be read back by `read`. |
| `print`     | `[*]`      | Much like `prin1`, except that the printed representation of *`obj`* is preceded by a newline and followed by a space. **(???)** |
| `mapcar `   | `map`      | "Maps" a *`fn`* through a *`list`*. This means hat the *`fn`* called is then sequentially applied to every index of the *`list`*. `[**]` |
| `mapc`      | `for-each` | Much like `map`/`mapcar`, except that the *`fn`* is applied from left-to-right on the indices of the *`list`*, with the result(s) of the applications discarded. The resulting value  is left unspecified. |

`[*]`: *This is such a bizarrely-specific function, that it's existence in any standard library is giving me an aneurysm, but it's easily defineable in Scheme, by yourself, not the goddamn stdlib*:

```scheme
(define (cl-print x)
  (newline)
  (write (string-append x " ")))
```

*To be continued...*
