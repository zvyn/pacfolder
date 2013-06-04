pkgname=pacfolder
_gitname=pacfolder
pkgver=c04223b
pkgrel=1
pkgdesc="Programm to generate a folder with subfolders for each package\
 managed by pacman containing symlinks to all files belonging to that package."
arch=('any')
url="https://github.com/zvynar/pacfolder"
license=('MIT')
depends=('pacman' 'python')
makedepends=('git')
source=('git://github.com/zvynar/pacfolder.git')
md5sums=('SKIP')

pkgver() {
  cd $_gitname
  # Use the tag of the last commit
  git describe --always | sed 's|-|.|g'
}

package() {
  install -Dm755 "$srcdir/$_gitname/pacfolder" "$pkgdir/usr/bin/pacfolder"
}
