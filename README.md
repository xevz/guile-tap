# guile-tap example

**guile-tap.scm** is a simple drop-in library for unit-testing programs developed with [GNU Guile](http://www.gnu.org/software/guile/). It implements the [Test Anything Protocol (TAP)](https://testanything.org/).
*guile-tap* is very minimalistic. You might prefer to use Mathieu Lirzin's new SRFI-64 Automake TAP integration (see [wedesoft/guile-testing](https://github.com/wedesoft/guile-testing) for an example on how to use it).

You can try out the example test script which uses [guile-tap.scm](guile-tap.scm) as follows:

```Shell
guile -L . test_example.scm
```

You can use Automake TAP support like this:

```Shell
make -f Makefile.dist
./configure
make check
```

It will give some errors to demonstrate the behaviour of the test script.

![See picture for output of 'make check'](guile-tap.png)

## External links

* [wedesoft/guile-tap](https://github.com/wedesoft/guile-tap/)
* [xevz/guile-tap](https://github.com/xevz/guile-tap/)
* [SRFI-64](http://srfi.schemers.org/srfi-64/srfi-64.html)
* [cuirass build automation server](https://notabug.org/mthl/cuirass) (see [build-aux/test-driver.scm](https://notabug.org/mthl/cuirass/src/master/build-aux/test-driver.scm))
