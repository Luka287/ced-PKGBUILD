# Maintainer: Luka287 <Luka287@proton.me>

pkgname=ced 
pkgver=0.6.0
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
	
	cmake -DCMAKE_BUILD_TYPE=Debug -G Ninja "-DCMAKE_PREFIX_PATH=/path/to/Qt;/path/to/llvm" .

	cmake --build .
}

package(){
	cd "$pkgname-$pkgver"

	install -Dm644 LICENSE "${pkgdir}/usr/share/licenses/${pkgname}/LICENSE"
	install -Dm644 README.md "${pkgdir}/usr/share/doc/${pkgname}/README.md"
	install -Dm644 ced.desktop "${pkgdir}/usr/share/applications/ced.desktop"

	install -Dm755 ced "${pkgdir}/usr/bin/ced"

	install -Dm644 config.json "${pkgdir}/etc/ced/config.json"
	install -Dm644 config.json "${pkgdir}/$HOME/.config/ced/config.json"

}


sha256sums=('9fc0ab12bad6927d6a286b560dccc6d9bf0a90debe4428ec8429d6987df86292')
