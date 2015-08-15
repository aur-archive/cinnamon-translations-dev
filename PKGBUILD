# $Id$
# Maintainer: Realex
# Based on cinnamon-translations PKGBUILD

_pkgname=cinnamon-translations
pkgname=${_pkgname}-dev
pkgver=35.ecbc249
pkgrel=1
pkgdesc="Translations for Cinnamon, Nemo, Cinnamon Control Center..."
arch=('any')
url="https://github.com/linuxmint/cinnamon-translations"
license=('GPL')
makedepends=('git')
conflicts=(${_pkgname})
provides=(${_pkgname})
source=("git://github.com/linuxmint/${_pkgname}.git")
sha256sums=('SKIP')

pkgver() {
  cd $_pkgname
  echo $(git rev-list --count master).$(git rev-parse --short master)
}

package() {
  cd ${srcdir}/${_pkgname}

  install -m 0755 -d ${pkgdir}/usr/share/cinnamon/locale/ 
  cp -Rp mo-export/* ${pkgdir}/usr/share/cinnamon/locale/
}
