ASCRIPT
=======

Open vSwitch command line helper.

The design referrs to Ethan's ovs-dev.py script.

Alex's ovs helper SCRIPT.


ascript [elog | vlog | kill | rmlog] [-d=DIR]

OPTIONS:

    elog:       emacs ovs-vswitchd.log
    vlog:       vi ovs-vswitchd.log
    rmlog:      rm ovs-vswitchd.log

    kill:       stop ovs.

[-d=DIR]

    -d=DIR:     specify where to put db, log, pid files.


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
    clean:      git clean -fx.
    mclean:     make clean.

    start:      run ovs.

EXTRA CONFIGS:

    -d=DIR:     specify where to put db, log, pid files.
    C=1:        use sparse.
    clang:      use clang.
    debug:      start ovs in debug mode.

EXAMPLES:

    ascript log
    ascript /root/ASCRIPT conf make clang
    ascript /root/ASCRIPT kernel C=1
    ascript /root/ASCRIPT start debug

NOTE:

    'all' will override other options.

Version 1.0