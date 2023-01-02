## Setup

# wxwidgets
cd wxWidgets-3.2.1
mkdir build-gtk
cd build-gtk
../configure --disable-shared --with-opengl --with-gtk=3 --prefix=$(pwd)
make -j4
export PATH=$PATH:/home/$USER/Dev/wxWidgets-3.2.1/build-gtk
(append export to "~/.bashrc")

# unused
// sudo make install
// sudo ldconfig

# build command
ccmake -G "Unix Makefiles" ..