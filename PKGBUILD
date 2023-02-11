# Maintainer: Luka287 <Luka287@proton.me>

pkgname=ced-git 
pkgver=0.4.0
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
	
}


sha256sums=('b0555239dedfc0ebc2d97b88d5661f9c7352bcb7c72380925f50868d9f3a278a')
