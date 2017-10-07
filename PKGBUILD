# This is an example PKGBUILD file. Use this as a start to creating your own,
# and remove these comments. For more information, see 'man PKGBUILD'.
# NOTE: Please fill out the license field for your package! If it is unknown,
# then please put 'unknown'.

# Maintainer: Your Name <youremail@domain.com>
pkgname=ctrl-capslock-swap-us-keymap
pkgver=1.0.0
pkgrel=1
pkgdesc='Swaps the left control and capslock key in the us keymap.'
url='https://github.com/isomarcte/ctrl-capslock-swap-us-keymap'
license=('BSD')
source=("https://github.com/isomarcte/${pkgname}/archive/${pkgver}.tar.gz")
md5sums=('0a997ebcdf37493126e1d4348ed8a12f')
sha1sums=('a5f82c513eceacbb745c73d5a5bd11d1cdaa2fce')
sha256sums=('d603ec7f76847c2f0279c224444480e703474370eac4872a997fa2432845c617')
sha384sums=('c80ad889a55f88c9e4bbb265177c478b6ecb4971ee7fd3df6b9780f886213cc3f7e38720c6adb288e40312e376eec389')
sha512sums=('da978792c71c08bdca4a7d82d06e6ed717ed4219104c8c178f51ce01ec40cf5e1353eae7a1d5466ed0b618900308fd5d9bc141b0062635fe5a4dfbbb6da38f01')
arch=('any')
depends=('kbd'
         'systemd')
makedepends=('gzip'
             'make')
install="${pkgname}.install"

package() {
    cd "$pkgname-$pkgver"

    local -r LICENSE_DIR="$pkgdir/usr/share/licenses/$pkgname/"

    install -d "$LICENSE_DIR"
    install -t "$LICENSE_DIR" LICENSE

    make DESTDIR="$pkgdir/" install
}
