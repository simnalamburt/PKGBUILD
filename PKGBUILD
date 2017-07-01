# Maintainer: Sven-Hendrik Haase <sh@lutzhaase.com>
# Contributor: Jan Koppe <post@jankoppe.de>

pkgname=yarn
pkgver=0.27.5
pkgrel=1
pkgdesc='Fast, reliable, and secure dependency management'
arch=(any)
url='https://yarnpkg.com'
license=('BSD')
depends=('nodejs')
source=("https://github.com/yarnpkg/yarn/releases/download/v$pkgver/yarn-v$pkgver.tar.gz")
sha512sums=('a21615f3bf4996d6e2dc84b54c3e9ca8a58143941a80771121f6eb6f5dcf8fd655e1c9b9420e7a0ab3a7c26ecd6bdd3790451d76435d7e3d6fbb5ba8ac729dbd')

package() {
  install -dm755  "$pkgdir"/usr/lib/node_modules/yarn
  cp -R "$srcdir"/dist/* "$pkgdir"/usr/lib/node_modules/yarn

  install -dm755 "$pkgdir"/usr/bin
  ln -s /usr/lib/node_modules/yarn/bin/yarn.js "$pkgdir"/usr/bin/yarn
  ln -s /usr/lib/node_modules/yarn/bin/yarn.js "$pkgdir"/usr/bin/yarnpkg

  install -Dm644 "$srcdir"/dist/LICENSE "$pkgdir/usr/share/licenses/$pkgname/LICENSE"
}
