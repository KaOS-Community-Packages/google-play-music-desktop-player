pkgname=google-play-music-desktop-player
pkgver=3.6.0
pkgrel=1
pkgdesc="An electron wrapper for Google Play Music"
arch=('x86_64')
url="https://github.com/MarshallOfSound/Google-Play-Music-Desktop-Player-UNOFFICIAL-"
license=('MIT')
depends=('gconf' 'gtk2' 'libxtst' 'nss' 'alsa-lib' 'libnotify' 'fontconfig')
sha256sums=('245566b56a7bd984381bbeab5ebf1a91e4f86f377af11d4181c5eeacb806c7cc')
source=("https://github.com/MarshallOfSound/Google-Play-Music-Desktop-Player-UNOFFICIAL-/releases/download/v${pkgver}/${pkgname}_${pkgver}_amd64.deb")

package() {
  tar -xf data.tar.xz -C "${pkgdir}"
  chmod -R 755 "$pkgdir/usr"
  rm -r $pkgdir/usr/share/{lintian,doc}
}
