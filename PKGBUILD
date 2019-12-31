# Maintainer: Yamada Hayao <shun819.mail@gmail.com>

pkgname=search-in-dir-git
pkgver=1.0
pkgrel=1
pkgdesc="ディレクトリの中のテキストファイルを検索します。"
arch=('any')
url=https://github.com/Hayao0819/search-in-dir
license=('MIT')
depends=('bash')
optdepends=()
source=("git+https://github.com/Hayao0819/search-in-dir.git")
md5sums=('SKIP')
conflicts=()

pkgver() {
  cd "search-in-dir"
  git describe --tags | sed 's/-/.r/; s/-g/./'
}
build () {
  cd "search-in-dir"
  rm -f README.md
  rm -f PKGBUILD
  rm -rf .git
  chmod 755 ./usr/bin/sid
  mv * ..
  cd ..
  rm -rf ./search-in-dir
}
package() {
    mkdir -p "$pkgdir"
    cp -r * "$pkgdir"
}

