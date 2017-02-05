pkgname=bomi
pkgver=0.19.2
_branch=development
pkgrel=3
pkgdesc="Powerful and easy-to-use GUI multimedia player based on mpv"
arch=('x86_64')
url="http://$pkgname-player.github.io"
license=('GPL')
install=$pkgname.install
depends=('qt5-base' 'qt5-declarative' 'qt5-x11extras' 'qt5-quickcontrols' 'icu'
         'libdvdread' 'libdvdnav' 'libcdio-paranoia' 'libcdio'
         'alsa-lib' 'pulseaudio' 'jack' 'libchardet' 'libbluray'
         'mpg123' 'libva' 'libgl' 'fribidi' 'libass' 'ffmpeg')
makedepends=('mesa' 'gcc' 'pkg-config' 'python3' 'qt5-tools')
optdepends=('youtube-dl: streaming website support including YouTube')
source=(https://github.com/ShalokShalom/bomi/archive/$_branch.zip)
md5sums=('deada47449228a5a99b41c05449904c2')

build() {
  cd "$srcdir/$pkgname-$_branch"
  ./configure --prefix=/usr --enable-jack --enable-cdda --enable-pulseaudio
  sed -i 's/--disable-cplayer/--disable-cplayer --disable-rubberband/g' build-mpv
  make
}

package() {
  cd "$srcdir/$pkgname-$_branch"
  make DEST_DIR=$pkgdir install
}
