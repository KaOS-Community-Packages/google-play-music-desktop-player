pkgname=google-play-music-desktop-player
pkgver=3.2.0
pkgrel=1
pkgdesc="An electron wrapper for Google Play Music"
arch=('x86_64')
url="https://github.com/MarshallOfSound/Google-Play-Music-Desktop-Player-UNOFFICIAL-"
license=('MIT')
depends=('gconf' 'gtk2' 'libxtst' 'nss' 'alsa-lib' 'libnotify' 'fontconfig')
install=google-play-music-desktop-player.install
sha256sums=('d93ca3870d025efbda3b9d0b4d4850177b1e3c14e33d77babdabcea13d416697')
source=("https://github.com/MarshallOfSound/Google-Play-Music-Desktop-Player-UNOFFICIAL-/releases/download/v${pkgver}/${pkgname}_${pkgver}_amd64.deb")


package() {
  tar -xf ${srcdir}/data.tar.xz -C "${pkgdir}"
  chmod -R 755 "$pkgdir/usr"
  sed -i  's/GNOME;GTK;Utility/Audio;Music;Player;AudioVideo/' "$pkgdir/usr/share/applications/$pkgname.desktop"
  rm -r $pkgdir/usr/share/lintian
}
