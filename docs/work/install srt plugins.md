    sudo apt install libsrt-dev

or

    git clone https://github.com/Haivision/srt.git 
    cd srt/ 
    git checkout v1.2.3 
    mkdir build
    cd build
    cmake ..
    make
    sudo make install
    sudo ldconfig


    git clone https://gitlab.freedesktop.org/gstreamer/gst-plugins-bad.git 
    cd gst-plugins-bad/ 
    git checkout 1.14.5 
    ./autogen.sh --with-srt
    meson builddir --prefix /usr
    ninja -C builddir ext/srt/libgstsrt.so.p/libgstsrt.so.symbols

The library is here   builddir/ext/srt/libgstsrt.so
copy it to /usr/lib/aarch64-linux-gnu/gstreamer-1.0/
