# Maintainer: lilydjwg <lilydjwg@gmail.com>

_gitname=python-romkan
pkgname=python-romkan-git
pkgver=20131017
pkgrel=1
pkgdesc="A Romaji/Kana conversion library for Python"
arch=('any')
url="http://pypi.python.org/pypi/romkan"
license=('BSD')
depends=('python' 'python-setuptools')
makedepends=('git')
source=("git://github.com/soimort/$_gitname.git")
md5sums=('SKIP')

pkgver() {
  cd "$srcdir/$_gitname"
  git log -1 --pretty='%cd' --date=short | tr -d '-'
}

package() {
  cd "$srcdir/$_gitname"
  python3 setup.py install --root="$pkgdir/" --optimize=1
}

