# Maintainer:  Alan Young <harleypig@harlepig.com>
# Contributor: Kyle Keen <keenerd@gmail.com>
# Contributor: Thomas Dziedzic < gostrc at gmail >

# Yes, this has been stolen whole from the original aur-git package.

pkgname=aur-git
pkgver=20140516
pkgrel=1
pkgdesc='ABS-like command line tool to sync with the AUR git repository'
arch=('any')
url='https://github.com/harleypig/aur'
license=('MIT')
makedepends=('git')
source=('git://github.com/harleypig/aur.git')
md5sums=('SKIP')

_gitname='aur'

pkgver() {
  cd "$_gitname"
  git show -s --format="%ci" HEAD | sed -e 's/-//g' -e 's/ .*//'
}


package() {
  cd "$_gitname"
  install -Dm755 aur "$pkgdir/usr/bin/aur"
  install -Dm644 LICENSE "$pkgdir/usr/share/licenses/aur-git/LICENSE"
}
