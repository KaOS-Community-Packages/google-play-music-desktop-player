pkgname=google-play-music-desktop-player
pkgver=3.0.0
pkgrel=2
pkgdesc="An electron wrapper for Google Play Music"
arch=('x86_64')
url="https://github.com/MarshallOfSound/Google-Play-Music-Desktop-Player-UNOFFICIAL-"
license=('MIT')
depends=('libnotify' 'alsa-lib' 'gconf' 'gtk2' 'nss')
install=google-play-music-desktop-player.install
sha256sums=('4994ca0f4a0b9c31fcfb719134fe801237cbf029e7a967c64d7c7ef9d8dfc55f')
source=("https://github.com/MarshallOfSound/Google-Play-Music-Desktop-Player-UNOFFICIAL-/releases/download/3.0.0/${pkgname}_${pkgver}_linux_amd64.deb")

package() {
  tar -xzf ${srcdir}/data.tar.gz -C "${pkgdir}"
  chmod -R 755 "$pkgdir/usr"
  sed -i  's/GNOME;GTK;Utility/Audio;Music;Player;AudioVideo/' "$pkgdir/usr/share/applications/$pkgname.desktop"
}
