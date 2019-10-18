# Maintainer: Tom Meyers tom@odex.be
pkgname=source-marking-system-git
pkgver=r6.e42f5be
pkgrel=1
pkgdesc="A tool to mark your source code with your copyright/license"
arch=(any)
url="https://github.com/F0xedb/source-marking-system"
_reponame="source-marking-system"
license=('MIT')

source=(
"git+https://github.com/F0xedb/source-marking-system.git")
md5sums=('SKIP')
makedepends=('git')

pkgver() {
  cd "$srcdir/$_reponame"
  printf "r%s.%s" "$(git rev-list --count HEAD)" "$(git rev-parse --short HEAD)"
}


build() {
    return 0;
}

package() {
        cd "$srcdir/$_reponame"
        install -Dm755 annotate "$pkgdir"/usr/bin/annotate
}