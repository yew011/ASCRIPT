ASCRIPT
=======

Open vSwitch command line helper.

The design referrs to Ethan's ovs-dev.py script.

Alex's ovs helper SCRIPT.



ascript [elog | vlog | kill | rmlog]

OPTIONS:
    elog:       emacs ovs-vswitchd.log.
    vlog:       vi ovs-vswitchd.log.
    rmlog:      rm ovs-vswitchd.log.
    etag:       create etags.

    kill:       stop ovs.



ascript [DIRECTORY] [OPTIONS] [EXTRA CONFIG...]

DIRECTORY:
    the path to ovs directory.

OPTIONS:
    all:        rebuild everything and start ovs.
    boot:       boot.sh.
    conf:       configure.
    kernel:     install kernel module.
    make:       make and make install.
    check:      make check -j8.

    rmmod:      rmmod k-module.
    gclean:     git clean -dfx.
    mclean:     make clean.
    dclean:     make distclean.

    start:      run ovs.
    debug:      start ovs in debug mode.

EXTRA CONFIGS:
    C=1:        use sparse.
    clang:      use clang.

EXAMPLES:
    ascript log
    ascript $PWD conf make clang
    ascript $PWD kernel C=1
    ascript $PWD start debug

NOTE:
    'all' will override other options.

Version 1.1