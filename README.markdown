What?
=====
A simple TAP implementation in (Guile) Scheme.

Why?
====
I wanted to experiment with Scheme a bit and unit testing with TAP is quite cool.

How?
====

    (use-modules (guile-tap))

	(planned-tests 3)

	(ok (= 1 1))
	(ok (not (null? '(21))))

	(diagnostics "Skip some tests...")
    (skip #t
     (list
       '(ok (= 1 1))
       '(ok (not (= 1 2))))
	 ; Optional reason
	 "A reason")

	(diagnostics "Bail out...")
	(bail-out!)

	(diagnostics "Todo is supported as well...")
	(todo
	 (list
	  '(ok (= 1 1)))
	 ; Optional note
	 "A note")

