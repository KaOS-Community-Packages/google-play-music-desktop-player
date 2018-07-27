pkgname=google-play-music-desktop-player
pkgver=4.6.1
pkgrel=1
pkgdesc="An electron wrapper for Google Play Music"
arch=('x86_64')
url="https://github.com/MarshallOfSound/Google-Play-Music-Desktop-Player-UNOFFICIAL-"
license=('MIT')
depends=('gconf' 'gtk2' 'libxtst' 'nss' 'alsa-lib' 'libnotify' 'fontconfig')
sha256sums=('4f48764eacd28370c3fadfc99540d62f9de78dfe3a5f566d6a296606bb13d637')
source=("https://github.com/MarshallOfSound/Google-Play-Music-Desktop-Player-UNOFFICIAL-/releases/download/v${pkgver}/${pkgname}_${pkgver}_amd64.deb")

package() {
  tar -xf data.tar.xz -C "${pkgdir}"
  chmod -R 755 "$pkgdir/usr"
  rm -r $pkgdir/usr/share/{lintian,doc}
}
