pkgname=google-play-music-desktop-player
pkgver=3.1.0
pkgrel=1
pkgdesc="An electron wrapper for Google Play Music"
arch=('x86_64')
url="https://github.com/MarshallOfSound/Google-Play-Music-Desktop-Player-UNOFFICIAL-"
license=('MIT')
depends=('libnotify' 'alsa-lib' 'gconf' 'gtk2' 'nss')
install=google-play-music-desktop-player.install
sha256sums=('75eaa01dae63ccc4caf4597278163f60bde47a384fbf35d33d196af2082c5db2')
source=("https://github.com/MarshallOfSound/Google-Play-Music-Desktop-Player-UNOFFICIAL-/releases/download/v${pkgver}/${pkgname}_${pkgver}_amd64.deb")


package() {
  tar -xf ${srcdir}/data.tar.xz -C "${pkgdir}"
  chmod -R 755 "$pkgdir/usr"
  sed -i  's/GNOME;GTK;Utility/Audio;Music;Player;AudioVideo/' "$pkgdir/usr/share/applications/$pkgname.desktop"
  rm -r $pkgdir/usr/share/lintian
}
