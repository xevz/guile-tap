TEST_EXTENSIONS = .scm
TESTS_ENVIRONMENT = LD_LIBRARY_PATH=$(top_builddir)/.libs:$(LD_LIBRARY_PATH)
SCM_LOG_COMPILE = $(GUILE) --no-auto-compile -L $(srcdir)
SCM_LOG_DRIVER = env AM_TAP_AWK='$(AWK)' $(SHELL) $(top_srcdir)/build-aux/tap-driver.sh --comments

TESTS = test_example.scm

EXTRA_DIST = Makefile.dist README.md configure.ac guile-tap.scm guile-tap.png $(TESTS)

CLEANFILES = *~ *.tmp *.log *.trs
