# p

A simple printing utility for Carp.

The basic idea is this: you have a program. It doesn’t work. You’re too lazy to
properly debug it. Instead, you want to use print debugging, like any normal
person. `p` is your friend!

It tries to be unintrusive, meaning it will return the value after printing it.
It also tries to be helpful, meaning it will print the file, line, and column
of where the call to `p` happens.

```clojure
; before
(if (= x 2)
  ; complicated thing
  ; other complicated thind
)

; after
; will print something like "REPL:4:15: 3" if x is 3
(load "https://github.com/hellerve/p@master")
(if (= (p x) 2)
  ; complicated thing
  ; other complicated thind
)
```

<br/>

Have fun!
