pkgname=google-play-music-desktop-player
pkgver=3.2.5
pkgrel=1
pkgdesc="An electron wrapper for Google Play Music"
arch=('x86_64')
url="https://github.com/MarshallOfSound/Google-Play-Music-Desktop-Player-UNOFFICIAL-"
license=('MIT')
depends=('gconf' 'gtk2' 'libxtst' 'nss' 'alsa-lib' 'libnotify' 'fontconfig')
sha256sums=('bcc6aff0c62054b38aae9f727ef389a41bfe95d5a1e5e202aebda087153db716')
source=("https://github.com/MarshallOfSound/Google-Play-Music-Desktop-Player-UNOFFICIAL-/releases/download/v${pkgver}/${pkgname}_${pkgver}_amd64.deb")

package() {
  tar -xf data.tar.xz -C "${pkgdir}"
  chmod -R 755 "$pkgdir/usr"
  rm -r $pkgdir/usr/share/{lintian,doc}
}
