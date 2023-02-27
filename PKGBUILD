# Maintainer: Luka287 <Luka287@proton.me>

pkgname=ced 
pkgver=0.7.4
pkgrel=1
epoch=
pkgdesc="Simple text editor made with Qt"
arch=('any')
url="https://github.com/Luka287/ced.git"
license=('GPL3')
groups=()
depends=(qt6-base)
makedepends=('cmake' 'ninja')
checkdepends=()
optdepends=()
provides=()
conflicts=()
replaces=()
backup=()
options=()
install=
changelog=
source=("https://github.com/Luka287/ced/archive/refs/tags/${pkgver}.tar.gz")
noextract=()
md5sums=()
validpgpkeys=()

build(){
	cd "$pkgname-$pkgver"
	
	cmake .

	cmake --build . --target all
}

package(){
	cd "$pkgname-$pkgver"

	install -Dm644 LICENSE "${pkgdir}/usr/share/licenses/${pkgname}/LICENSE"
	install -Dm644 README.md "${pkgdir}/usr/share/doc/${pkgname}/README.md"
	install -Dm644 ced.desktop "${pkgdir}/usr/share/applications/ced.desktop"

	install -Dm755 ced "${pkgdir}/usr/bin/ced"

	install -Dm644 config.json "${pkgdir}/etc/ced/config.json"
	install -Dm666 config.json "${pkgdir}/$HOME/.config/ced/config.json"

	install -Dm644 ced.png "${pkgdir}/usr/share/picmaps/ced.png"
}


sha256sums=('5aa1feb3d95e5161e9740d351020f81f6ecb60f6c2dbce7cceb0e9a04519fa3a')
