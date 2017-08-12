pkgname=macchanger
pkgver=1.7.0
pkgrel=2
pkgdesc="A small utility to change your NIC's MAC address"
arch=('x86_64')
#url="http://ftp.gnu.org/gnu/macchanger"
url="http://www.gnu.org/software/macchanger"
license=('GPL')
depends=('glibc')
source=("https://github.com/alobbs/macchanger/archive/$pkgver.tar.gz")
md5sums=('ebd3c24360454b2684c39d89dcaabac8')

build() {
  cd "${srcdir}/${pkgname}-${pkgver}"
  ./autogen.sh
  ./configure --prefix=/usr \
              --mandir=/usr/share/man \
              --infodir=/usr/share/info
  make
}

package() {
  cd "${srcdir}/${pkgname}-${pkgver}"

  make DESTDIR="${pkgdir}" install
}
