# Emacs build notes - macOS

## To build emacs-30 branch on macOS 15.1.1 using Homebrew libs

    brew install autoconf automake lcms2 librsvg texinfo gnutls # and probably some other packages
    export PATH="/usr/local/opt/texinfo/bin:$PATH"
    rm -fr emacs-30-build && mkdir emacs-30-build && cd emacs-30 && ./autogen.sh && cd ../emacs-30-build && ../emacs-30/configure --with-ns && nice make -j16 && make install
