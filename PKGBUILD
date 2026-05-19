# Maintainer: Jose Dragic <corelinuxx@gmail.com>

pkgname=core-rate-mirrors
pkgver=23
pkgrel=1
# groups=(cachyos)
arch=('any')
install=$pkgname.install
url="https://github.com/archlatam/core-rate-mirrors.git"
license=(GPL-1.0-only)
pkgdesc='Core - Rate mirrors service'
depends=(rate-mirrors)
source=(
  core-rate-mirrors
  core-rate-mirrors.service
  core-rate-mirrors.timer
  core-rate-mirrors.hook
)
sha256sums=('c8eefdede7b115ee7f4a59d6f631e491a0698c3a930c2fc2d2e9e710b4feaad2'
  '12e68f37b48f69050d65d4bbb82509756185fad68ae31f842a4c72d2e8957082'
  'e4f021419c508c6474aba175d131f0a98620b7736aa1f3daefc4c44f3c8d0f81'
  'acc2a023b3daee3c1e141c76baa149a5e21ee289a4745535c7f1ac08d3b9365c')

package() {
  install -Dm755 "$pkgname" "$pkgdir/usr/bin/$pkgname"
  install -Dm644 "$pkgname.service" "$pkgdir/usr/lib/systemd/system/$pkgname.service"
  install -Dm644 "$pkgname.timer" "$pkgdir/usr/lib/systemd/system/$pkgname.timer"
  install -Dm644 "$pkgname.hook" "$pkgdir/usr/share/libalpm/hooks/$pkgname.hook"
}
