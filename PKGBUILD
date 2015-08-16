# Contributor: Michael Seiwald <michael@mseiwald.at>
# Maintainer: Dmitry Korzhevin <dkorzhevin at gmail dot com>
pkgname=networkmanager-strongswan
_pkgname=NetworkManager-strongswan
pkgver=1.3.0
pkgrel=2
pkgdesc="strongswan NetworkManager plugin"
arch=('i686' 'x86_64')
url="http://wiki.strongswan.org/projects/strongswan/wiki/NetworkManager"
license=('GPL')
groups=()
depends=(networkmanager strongswan libgnomeui)
makedepends=()
checkdepends=()
optdepends=()
provides=()
conflicts=()
replaces=()
backup=()
options=()
install=
#changelog=
source=(http://download.strongswan.org/NetworkManager/$_pkgname-$pkgver.tar.gz)
noextract=()
md5sums=('215f1d3b7b65be236b86bf30b6a4615b')

build() {
  cd "$srcdir/$_pkgname-$pkgver"
  ./configure --sysconfdir=/etc --prefix=/usr --libexecdir=/usr/lib --with-charon=/usr/lib/strongswan/charon CFLAGS="$CFLAGS -Wno-error=unused-local-typedefs"
  make
}

package() {
  cd "$srcdir/$_pkgname-$pkgver"
  make DESTDIR="$pkgdir" install
  #make install
}

# vim:set ts=2 sw=2 et:
