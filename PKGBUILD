# $Id$
# Maintainer: Chupligin Sergey (NeoChapay) <neochapay@gmail.com>

pkgname=glacier-packagemanager
pkgver=0.4.2
pkgrel=1
pkgdesc="Glacier package manager"
arch=('x86_64' 'aarch64')
url="https://github.com/nemomobile-ux/glacier-packagemanager"
license=('LGPL-2.1')
depends=('libpamac' 'qt5-glacier-app' 'glacier-polkit-agent')
makedepends=( 'cmake' 'qt5-tools')
source=("${url}/archive/refs/tags/$pkgver.tar.gz")
sha256sums=('736e0852835aebb2b68e36bb6ada1d71ab2736c414564e6df937036ae8464b05')

build() {
    cd $pkgname-$pkgver
    cmake \
        -DCMAKE_INSTALL_PREFIX:PATH='/usr'
    make all
}


package() {
    cd $pkgname-$pkgver
    make DESTDIR="$pkgdir" install
}
