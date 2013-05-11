# Maintainer: Jakub Klinkovský <kuba.klinkovsky@gmail.com>

pkgname=tinyterm-git
_pkgname=tinyterm
pkgver=v0.1beta.6.g25da896
pkgrel=1
pkgdesc="Very lightweight terminal emulator based on VTE (fork of tinyterm-svn package)"
arch=('i686' 'x86_64')
url="https://github.com/lahwaacz/tinyterm"
license=('MIT')
depends=('vte')
makedepends=('git')
source=('git://github.com/lahwaacz/tinyterm.git')
md5sums=('SKIP')

pkgver() {
  cd "$_pkgname"
  git describe --always | sed 's|-|.|g'
}

build() {
  cd "$_pkgname"
  make
}

package() {
  cd "$_pkgname"
  make DESTDIR="$pkgdir" install
  install -Dm644 LICENSE "$pkgdir/usr/share/licenses/$pkgname/LICENSE"
}

# vim:set ts=2 sw=2 et:
