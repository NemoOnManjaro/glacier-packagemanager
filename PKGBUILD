# $Id$
# Maintainer: Chupligin Sergey (NeoChapay) <neochapay@gmail.com>

pkgname=glacier-packagemanager
pkgver=0.4.1
pkgrel=1
pkgdesc="Glacier package manager"
arch=('x86_64' 'aarch64')
url="https://github.com/nemomobile-ux/glacier-packagemanager"
license=('LGPL-2.1')
depends=('libpamac' 'qt5-glacier-app')
makedepends=( 'cmake' 'qt5-tools')
source=("${url}/archive/refs/tags/$pkgver.tar.gz")
sha256sums=('c506d09ab444263a90bc9ac96b0d048e4a0835c981149afcafa4a28e2e788fc2')

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
