# Maintainer: uberushaximus <uberushaximus AT gmail DOT com>

_gemname=whistlepig
pkgname=ruby-$_gemname
pkgver=0.12
pkgrel=1
pkgdesc='a minimalist realtime full-text search index'
arch=(any)
url='http://masanjin.net/whistlepig'
license=(custom:whistlepig)
depends=(ruby)
source=(https://rubygems.org/downloads/$_gemname-$pkgver.gem)
noextract=($_gemname-$pkgver.gem)
sha1sums=('cc2f2e959dc2671f718a8bf749ae172f1048d526')

package() {
  local _gemdir="$(ruby -e'puts Gem.default_dir')"
  gem install --ignore-dependencies --no-user-install -i "$pkgdir/$_gemdir" -n "$pkgdir/usr/bin" $_gemname-$pkgver.gem
  rm "$pkgdir/$_gemdir/cache/$_gemname-$pkgver.gem"
  install -D -m644 "$pkgdir/$_gemdir/gems/$_gemname-$pkgver/COPYING" "$pkgdir/usr/share/licenses/$pkgname/LICENSE"
}
