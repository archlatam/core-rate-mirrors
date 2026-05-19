# Maintainer: Jose Dragic <corelinuxx@gmail.com>

pkgname=core-rate-mirrors
pkgver=1
pkgrel=1
arch=('any')
url="https://github.com/archlatam/core-rate-mirrors"
license=('GPL-2.0-or-later')
pkgdesc='Core - Rate mirrors service'
depends=('rate-mirrors')
install="$pkgname.install"

source=(
  "$pkgname"
  "$pkgname.service"
  "$pkgname.timer"
  "$pkgname.hook"
)

sha256sums=('fc2cc2d83e7db69a9e304ebe9d48dab20992b53a1d558685b225a3bdf6805f09'
            '12e68f37b48f69050d65d4bbb82509756185fad68ae31f842a4c72d2e8957082'
            'e4f021419c508c6474aba175d131f0a98620b7736aa1f3daefc4c44f3c8d0f81'
            'acc2a023b3daee3c1e141c76baa149a5e21ee289a4745535c7f1ac08d3b9365c')

package() {
  install -Dm755 "$pkgname" \
    "$pkgdir/usr/bin/$pkgname"

  install -Dm644 "$pkgname.service" \
    "$pkgdir/usr/lib/systemd/system/$pkgname.service"

  install -Dm644 "$pkgname.timer" \
    "$pkgdir/usr/lib/systemd/system/$pkgname.timer"

  install -Dm644 "$pkgname.hook" \
    "$pkgdir/usr/share/libalpm/hooks/$pkgname.hook"
}
