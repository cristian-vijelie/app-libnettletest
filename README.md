# Unikraft LibNettle Test Application

This application tests the correct functioning of the nettle cryptographic
library.

The application requires newlib and nettle to work. Also, the LIBNETTLE_TEST
option should be selected for nettle in menuconfig.

You should configure UK_ROOT and UK_LIBS, in Makefile, acording to your setup.

Known issues:
*   On linuxu platform, test suite 0 will make unikraft crash. Test suites
    are made so unikraft won't crash.
*   9pfs is required to run for the yarrow test, as it reads the golden-bug.txt
    file (build/libnettle/origin/nettle-3.6/testsuite) - currently not working 
    at all.
