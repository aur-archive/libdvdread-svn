# Maintainer: Lukas Jirkovsky <l.jirkovsky@gmail.com>
pkgname=libdvdread-svn
pkgver=1257
pkgrel=1
pkgdesc="A simple foundation for reading DVD video disks"
arch=('i686' 'x86_64')
url="http://dvdnav.mplayerhq.hu/"
license=('GPL2')
depends=()
makedepends=('subversion')
provides=('libdvdread')
conflicts=('libdvdread')
options=(!libtool)
source=('libdvdread::svn+svn://svn.mplayerhq.hu/dvdnav/trunk/libdvdread')
md5sums=('SKIP')

pkgver() {
  cd "$srcdir/libdvdread"
  svnversion | tr -d [A-z]
}

build() {
  cd "$srcdir/libdvdread"

  ./autogen.sh --prefix=/usr
  make
}

package() {
  cd "$srcdir/libdvdread"

  make DESTDIR="$pkgdir" install
}
