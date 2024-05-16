# $Id$
# Maintainer: Chupligin Sergey (NeoChapay) <neochapay@gmail.com>

pkgname=glacier-packagemanager
pkgver=0.5
pkgrel=1
pkgdesc="Glacier package manager"
arch=('x86_64' 'aarch64')
url="https://github.com/nemomobile-ux/glacier-packagemanager"
license=('LGPL-2.1')
depends=('libpamac' 'qt6-glacier-app')
makedepends=( 'cmake' 'qt6-tools')
source=("${url}/archive/refs/tags/$pkgver.tar.gz")
sha256sums=('5ca527d005debeeae8a6931be6090cc6514493432e380b4848ad68811d904f57')

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
