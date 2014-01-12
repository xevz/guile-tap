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
(skip #t
  (list
    '(ok (= 1 1))
    '(ok (not (= 1 2))))
  ; Optional reason
  "A reason")

(diagnostic "Bail out...")
(bail-out!)

(diagnostic "Todo is supported as well...")
(todo
  (list
    '(ok (= 1 1)))
    ; Optional note
  "A note")

(ok (throws? (/ 1 0)) "Test for exception")
```
