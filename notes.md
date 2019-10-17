To build emacs-26.3 on 10.14 using Homebrew libs:

    cp /Library/Developer/CommandLineTools/Packages/macOS_SDK_headers_for_macOS_10.14.pkg ~/Desktop

Run pkg from desktop

    (PATH=`pwd`/build-tools:"$PATH" && rm -fr emacs-build && mkdir emacs-build && cd emacs && ./autogen.sh && cd ../emacs-build && ../emacs/configure --with-ns && nice make -j8 && make install)

```
$ otool -L /Applications/Emacs.app/Contents/MacOS/Emacs
/Applications/Emacs.app/Contents/MacOS/Emacs:
	/System/Library/Frameworks/AppKit.framework/Versions/C/AppKit (compatibility version 45.0.0, current version 1671.60.107)
	/System/Library/Frameworks/IOKit.framework/Versions/A/IOKit (compatibility version 1.0.0, current version 275.0.0)
	/usr/local/opt/jpeg/lib/libjpeg.9.dylib (compatibility version 13.0.0, current version 13.0.0)
	/usr/lib/libxml2.2.dylib (compatibility version 10.0.0, current version 10.9.0)
	/usr/lib/libncurses.5.4.dylib (compatibility version 5.4.0, current version 5.4.0)
	/usr/local/opt/gnutls/lib/libgnutls.30.dylib (compatibility version 54.0.0, current version 54.2.0)
	/usr/lib/libz.1.dylib (compatibility version 1.0.0, current version 1.2.11)
	/usr/lib/libSystem.B.dylib (compatibility version 1.0.0, current version 1252.250.1)
	/System/Library/Frameworks/CoreFoundation.framework/Versions/A/CoreFoundation (compatibility version 150.0.0, current version 1575.17.0)
	/System/Library/Frameworks/CoreGraphics.framework/Versions/A/CoreGraphics (compatibility version 64.0.0, current version 1265.9.0)
	/System/Library/Frameworks/CoreText.framework/Versions/A/CoreText (compatibility version 1.0.0, current version 1.0.0)
	/System/Library/Frameworks/Foundation.framework/Versions/C/Foundation (compatibility version 300.0.0, current version 1575.17.0)
	/usr/lib/libobjc.A.dylib (compatibility version 1.0.0, current version 228.0.0)
$ ls -l build-tools
total 0
lrwxr-xr-x  1 francis  staff  22 13 Oct  2017 aclocal -> /usr/local/bin/aclocal
lrwxr-xr-x  1 francis  staff  27 13 Oct  2017 aclocal-1.15 -> /usr/local/bin/aclocal-1.15
lrwxr-xr-x  1 francis  staff  23 13 Oct  2017 autoconf -> /usr/local/bin/autoconf
lrwxr-xr-x  1 francis  staff  25 13 Oct  2017 autoheader -> /usr/local/bin/autoheader
lrwxr-xr-x  1 francis  staff  23 13 Oct  2017 autom4te -> /usr/local/bin/autom4te
lrwxr-xr-x  1 francis  staff  23 13 Oct  2017 automake -> /usr/local/bin/automake
lrwxr-xr-x  1 francis  staff  28 13 Oct  2017 automake-1.15 -> /usr/local/bin/automake-1.15
lrwxr-xr-x  1 francis  staff  25 13 Oct  2017 autoreconf -> /usr/local/bin/autoreconf
lrwxr-xr-x  1 francis  staff  23 13 Oct  2017 autoscan -> /usr/local/bin/autoscan
lrwxr-xr-x  1 francis  staff  25 13 Oct  2017 autoupdate -> /usr/local/bin/autoupdate
lrwxr-xr-x  1 francis  staff  31 16 May  2018 info -> /usr/local/opt/texinfo/bin/info
lrwxr-xr-x  1 francis  staff  39 16 May  2018 install-info -> /usr/local/opt/texinfo/bin/install-info
lrwxr-xr-x  1 francis  staff  35 16 May  2018 makeinfo -> /usr/local/opt/texinfo/bin/makeinfo
lrwxr-xr-x  1 francis  staff  38 16 May  2018 pdftexi2dvi -> /usr/local/opt/texinfo/bin/pdftexi2dvi
lrwxr-xr-x  1 francis  staff  35 16 May  2018 pod2texi -> /usr/local/opt/texinfo/bin/pod2texi
lrwxr-xr-x  1 francis  staff  35 16 May  2018 texi2any -> /usr/local/opt/texinfo/bin/texi2any
lrwxr-xr-x  1 francis  staff  35 16 May  2018 texi2dvi -> /usr/local/opt/texinfo/bin/texi2dvi
lrwxr-xr-x  1 francis  staff  35 16 May  2018 texi2pdf -> /usr/local/opt/texinfo/bin/texi2pdf
lrwxr-xr-x  1 francis  staff  35 16 May  2018 texindex -> /usr/local/opt/texinfo/bin/texindex
```
