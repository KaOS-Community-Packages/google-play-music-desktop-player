pkgname=google-play-music-desktop-player
pkgver=4.6.1
pkgrel=2
pkgdesc="An electron wrapper for Google Play Music"
arch=('x86_64')
url="https://github.com/MarshallOfSound/Google-Play-Music-Desktop-Player-UNOFFICIAL-"
license=('MIT')
depends=('gconf' 'gtk2' 'libxtst' 'nss' 'alsa-lib' 'libnotify' 'fontconfig')
sha256sums=('7a467be7a6fe0ba92017ccd0b73769c962e9d13e4f5d3fade619a3148fe3b0fc')
source=("https://2838-40008106-gh.circle-artifacts.com/0/home/circleci/project/dist/installers/debian/${pkgname}_${pkgver}_amd64.deb")

package() {
  tar -xf data.tar.xz -C "${pkgdir}"
  chmod -R 755 "$pkgdir/usr"
  rm -r $pkgdir/usr/share/{lintian,doc}
}
