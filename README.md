# guile-tap

**guile-tap.scm** is a simple drop-in library for unit-testing programs developed with [GNU Guile](http://www.gnu.org/software/guile/). It implements the [Test Anything Protocol (TAP)](https://testanything.org/).

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

## External links

* [wedesoft/guile-tap](https://github.com/wedesoft/guile-tap/)).
* [xevz/guile-tap](https://github.com/xevz/guile-tap/).
