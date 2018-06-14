pkgname=st
pkgver=0.8.1
pkgrel=1
epoch=
pkgdesc=""
arch=('x86_64')
url="st.suckless.org"
license=('MIT')
groups=()
depends=('libx11' 'xorgproto' 'libxft' 'fontconfig' 'freetype2' 'ttf-inconsolata')
makedepends=('pkgconf')
checkdepends=()
optdepends=()
provides=()
conflicts=()
replaces=()
backup=()
options=()
install=
changelog=
source=("dl.suckless.org/st/$pkgname-$pkgver.tar.gz"
        "my_changes.diff")
noextract=()
sha256sums=('c4fb0fe2b8d2d3bd5e72763e80a8ae05b7d44dbac8f8e3bb18ef0161c7266926'
            'SKIP')
validpgpkeys=()

prepare() {
	cd "$pkgname-$pkgver"
	patch < ../my_changes.diff
}

build() {
	cd "$pkgname-$pkgver"
	make clean all
}


package() {
	cd "$pkgname-$pkgver"
	make DESTDIR="$pkgdir/" install
}
