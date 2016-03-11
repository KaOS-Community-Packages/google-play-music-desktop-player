pkgname=google-play-music-desktop-player
pkgver=3.0.1
pkgrel=1
pkgdesc="An electron wrapper for Google Play Music"
arch=('x86_64')
url="https://github.com/MarshallOfSound/Google-Play-Music-Desktop-Player-UNOFFICIAL-"
license=('MIT')
depends=('libnotify' 'alsa-lib' 'gconf' 'gtk2' 'nss')
install=google-play-music-desktop-player.install
sha256sums=('347d001753d88478b53a5f3b4eaa1434f8e39ed6a2f3ca16ce33060b2629898f')
source=("https://github.com/MarshallOfSound/Google-Play-Music-Desktop-Player-UNOFFICIAL-/releases/download/${pkgver}/${pkgname}_${pkgver}_amd64.deb")


package() {
  tar -xf ${srcdir}/data.tar.xz -C "${pkgdir}"
  chmod -R 755 "$pkgdir/usr"
  sed -i  's/GNOME;GTK;Utility/Audio;Music;Player;AudioVideo/' "$pkgdir/usr/share/applications/$pkgname.desktop"
}
