pkgname=dmenu
pkgver=0.9
pkgrel=4
pkgdesc='A simple virtual terminal emulator for X.'
arch=('i686' 'x86_64' 'armv7h' 'aarch64')
license=('MIT')
depends=(libxft harfbuzz)
url=https://dmenu.suckless.org
source=(https://github.com/oregone1/dmenu-flexipatch/archive/refs/heads/master.tar.gz)

sha256sums=('')
_sourcedir=dmenu-flexipatch-master

build() {
  make -C "$_sourcedir" 
}

package() {
  local shrdir="$pkgdir/usr/share"
  make -C "$_sourcedir" PREFIX=/usr DESTDIR="$pkgdir" install
}
