# Maintainer: Brandon Invergo <brandon@invergo.net>
pkgname=paperq
pkgver=1.2.3
pkgrel=1
pkgdesc="A tool for managing a reading queue for academic literature"
arch=('any')
url="http://paperq.invergo.net/"
license=('GPL3')
depends=('bash' 'libunistring' 'btparse')
optdepends=('zeptodb: caching of bibliographic information'
    'cups: printing support')
source=("http://paperq.invergo.net/download/$pkgname-$pkgver.tar.gz")
md5sums=('9dc5c96922788559c024f6a6ef09b829')

build() {
	cd "$srcdir/$pkgname-$pkgver"
	./configure --prefix=/usr
	make
}

package() {
	cd "$srcdir/$pkgname-$pkgver"
	make DESTDIR="$pkgdir/" install
}
