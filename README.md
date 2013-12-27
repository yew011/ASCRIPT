ASCRIPT
=======

Open vSwitch command line helper.

The design referrs to Ethan's ovs-dev.py script.

Alex's ovs helper SCRIPT.

ascript [OPTIONS] [DIRECTORY] [EXTRA CONFIG...]

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
    ascript conf make $PWD clang
    ascript kernel $PWD C=1
    ascript start $PWD debug

Version 1.0
