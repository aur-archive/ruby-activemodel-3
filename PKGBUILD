# Generated by gem2arch (https://github.com/anatol/gem2arch)
# Maintainer: Anatol Pomozov <anatol.pomozov@gmail.com>

_gemname=activemodel
pkgname=ruby-$_gemname-3
pkgver=3.2.21
pkgrel=1
pkgdesc='A toolkit for building modeling frameworks (part of Rails).'
arch=(any)
url='http://www.rubyonrails.org'
license=(MIT)
depends=(ruby ruby-activesupport-3 ruby-builder-3.0)
options=(!emptydirs)
source=(https://rubygems.org/downloads/$_gemname-$pkgver.gem)
noextract=($_gemname-$pkgver.gem)
sha1sums=('aaf186bc935b66e52e43a5e5c8b0af37b0444ccc')

package() {
  local _gemdir="$(ruby -e'puts Gem.default_dir')"
  gem install --ignore-dependencies --no-user-install -i "$pkgdir/$_gemdir" -n "$pkgdir/usr/bin" $_gemname-$pkgver.gem
  rm "$pkgdir/$_gemdir/cache/$_gemname-$pkgver.gem"
  install -D -m644 "$pkgdir/$_gemdir/gems/$_gemname-$pkgver/MIT-LICENSE" "$pkgdir/usr/share/licenses/$pkgname/MIT-LICENSE"
}
