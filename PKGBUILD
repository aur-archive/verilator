# Maintainer: kfgz <kfgz at interia dot pl>
# Contributor: Chris Schwaab <christopher dot schwaab at gmail com>
# Contributor: Laszlo Papp <djszapi at gmail com>

pkgname=verilator
pkgver=3.868
pkgrel=1
pkgdesc="A fast simulator for synthesizeable Verilog"
arch=('i686' 'x86_64')
url="http://www.veripool.org/wiki/verilator"
license=('GPL')
depends=('gcc-libs')
source=(http://www.veripool.org/ftp/${pkgname}-${pkgver}.tgz)
md5sums=('678141acd579013e94c27194683879fd')

build() {
  cd "${srcdir}"/${pkgname}-${pkgver}
  ./configure --prefix=/usr
  make
}

package() {
  cd "${srcdir}"/${pkgname}-${pkgver}
  make DESTDIR="${pkgdir}" install
}
