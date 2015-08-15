# Modified from original gmpc pkgbuild created by tobias <tobias@archlinux.org>
# Contributor: Lukas Miczka <lukascpu@gmail.com>

pkgname=gmpc-magnatune
pkgver=11.8.16
pkgrel=1
pkgdesc="A plugin that allows you to browse magnatune and preview music."
arch=(i686 x86_64)
url="http://sarine.nl/gmpc/"
license="GPL"
depends=("libmpd>=${pkgver}" "gmpc>=${pkgver}" "libxml2" "intltool>=0.21")
source=(http://download.sarine.nl/Programs/gmpc/${pkgver}/${pkgname}-${pkgver}.tar.gz)
sha1sums=('77df7b82fb8aa939a61b7b4d5a40d8a6c24d9e8f')

build() {
  cd ${startdir}/src
  tar xzf ${pkgname}-${pkgver}.tar.gz 
  cd $startdir/src/$pkgname-$pkgver
  ./configure --prefix=/usr
  make || return 1
  make DESTDIR=$pkgdir install
}

