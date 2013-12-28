ASCRIPT
=======

Open vSwitch command line helper.

The design referrs to Ethan's ovs-dev.py script.

Alex's ovs helper SCRIPT.

ascript [DIRECTORY] [OPTIONS] [EXTRA CONFIG...]

DIRECTORY:

    the path to ovs directory.

OPTIONS:

    all:        rebuild everything and start ovs.
    boot:       boot.sh.
    conf:       configure.
    kernel:     install kernel module.
    make:       make and make install.
    elog:       emacs ovs-vswitchd.log
    vlog:       vi ovs-vswitchd.log
    check:      make check -j8.

    rmmod:      rmmod k-module.
    clean:      git clean -fx.
    mclean:     make clean.

    run:        run ovs.
    kill:       stop ovs.

EXTRA CONFIGS:

    C=1:        use sparse.
    clang:      use clang.
    debug:      start ovs in debug mode.

EXAMPLES:

    ascript log
    ascript /root/ASCRIPT conf make /root/ASCRIPT clang
    ascript /root/ASCRIPT kernel C=1
    ascript /root/ASCRIPT start debug

NOTE:

    'all' and 'elog'/'vlog' will override other options.

Version 1.0