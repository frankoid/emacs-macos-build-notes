# Emacs build notes - macOS

## To build emacs-28 branch on 12.2.1 using Homebrew libs

    brew install lcms2 librsvg # and probably some other packages

    rm -fr emacs-28-build && mkdir emacs-28-build && cd emacs-28 && ./autogen.sh && cd ../emacs-28-build && ../emacs-28/configure --with-ns && nice make -j16 && make install
