# palera1n-iOS16-iboot-fix
Fix the Jailbreak injector error in Palera1n on iOS16.X devices (iboot)


On your Linux Computer, open a new XFCE4 terminal window and paste all commands bellow. 1 by 1 and in same order!




sudo apt-get update

sudo apt-get install build-essential

sudo apt-get install pkg-config

sudo apt-get install checkinstall

sudo apt-get install git

sudo apt-get install autoconf

sudo apt-get install automake

sudo apt-get install libtool-bin

sudo apt-get install libplist-dev

sudo apt-get install libusbmuxd-dev

sudo apt-get install libimobiledevice-glue-dev

sudo apt-get install libssl-dev

sudo apt-get install usbmuxd

sudo apt-get install doxygen	

sudo apt-get install cython



sudo git clone https://github.com/libimobiledevice/libimobiledevice.git

cd libimobiledevice

sudo ./autogen.sh

sudo make

sudo make install

sudo ./autogen.sh --prefix=/opt/local --enable-debug

sudo make

sudo make install



cd ..

sudo git clone https://github.com/libimobiledevice/libimobiledevice-glue.git

cd libimobiledevice-glue

sudo ./autogen.sh

sudo make

sudo make install

sudo ./autogen.sh --prefix=/opt/local

sudo make

sudo make install



cd ..

cd libimobiledevice

sudo ./autogen.sh --prefix=/opt/local --enable-debug

sudo make

sudo make install

sudo ./autogen.sh --with-gnutls

sudo ./autogen.sh --with-mbedtls mbedtls_INCLUDES=/opt/local/include mbedtls_LIBDIR=/opt/local/lib



cd ..

sudo git clone --recursive https://github.com/Italogc/usbmuxd2

sudo apt-get update

sudo apt-get upgrade

exit

