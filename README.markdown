What?
=====
A simple TAP implementation in (Guile) Scheme.

Why?
====
I wanted to experiment with Scheme a bit and unit testing with TAP is quite cool.

How?
====

```Scheme
(use-modules (guile-tap))
(planned-tests 3)
(ok (= 1 1))
(ok (not (null? '(21))))
(diagnostic "Skip some tests...")
(skip (= 1 1))
(skip (not (= 1 2)) "A description")
(diagnostic "Todo is supported as well...")
(todo (= 1 2) "A note")
(ok (throws? (/ 1 0)) "Test for exception")
```
