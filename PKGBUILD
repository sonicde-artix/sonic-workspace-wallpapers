# Maintainer: artist for Artix Linux

pkgname=sonic-workspace-wallpapers
pkgver=6.6.5
pkgrel=1
_commit="9402eca9b8b38399e24da784a50dc03e51fd4a70"
pkgdesc='Additional wallpapers for the Sonic Workspace'
arch=(any)
url='https://github.com/Sonic-DE/sonic-workspace-wallpapers'
license=(LGPL)
makedepends=(extra-cmake-modules qt5-base)
groups=(sonicde)
conflicts=(plasma-workspace-wallpapers)
provides=(plasma-workspace-wallpapers)
replaces=(plasma-workspace-wallpapers)
makedepends+=(git)
source=("$pkgname-$pkgver::git+$url.git#commit=$_commit")

build() {
  cmake -B build -S $pkgname-$pkgver \
    -DBUILD_TESTING=OFF
  cmake --build build
}

package() {
  DESTDIR="$pkgdir" cmake --install build
}

sha256sums=('e3aaacfadbc5954fa5ed17362d52c4982ee2de44351838021c4a6f93dbe21292')

