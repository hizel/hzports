Hz PORTS
========

::

    cd /usr/ports
    git clone git://github.com/hizel/hzports.git
    echo 'SUBDIR += hzports' >> Makefile.local
    cd hzports/mod_gnutls/ && make install clean
