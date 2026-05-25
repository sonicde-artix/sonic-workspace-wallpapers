# Maintainer: callmetango
# Contributor: artist <artist@artixlinux.org>

pkgname=sonic-workspace-wallpapers
pkgver=6.6.5
pkgrel=2
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
sha256sums=('0440c2f0719f10db3cbd7a163ad3830e8586f6e4158c128780e7b9814d0bf46e')

build() {
  cmake -B build -S $pkgname-$pkgver \
    -DBUILD_TESTING=OFF
  cmake --build build
}

package() {
  DESTDIR="$pkgdir" cmake --install build
}
