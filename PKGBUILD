# Maintainer: callmetango
# Contributor: artist <artist@artixlinux.org>

pkgname=sonic-workspace-wallpapers
pkgver=6.6.5
pkgrel=1
pkgdesc='Additional wallpapers for the Sonic Workspace'
arch=(any)
url='https://github.com/Sonic-DE/sonic-workspace-wallpapers'
license=(LGPL)
makedepends=(extra-cmake-modules qt5-base)
groups=(sonicde)
conflicts=(plasma-workspace-wallpapers)
replaces=(plasma-workspace-wallpapers)
provides=(plasma-workspace-wallpapers)
source=("$pkgname-$pkgver.tar.gz::${url}/archive/refs/tags/${pkgver}.tar.gz")
sha256sums=('e3aaacfadbc5954fa5ed17362d52c4982ee2de44351838021c4a6f93dbe21292')

build() {
  cmake -B build -S $pkgname-$pkgver \
    -DBUILD_TESTING=OFF
  cmake --build build
}

package() {
  DESTDIR="$pkgdir" cmake --install build
}
