# Maintainer: Luka287 <Luka287@proton.me>


pkgname=ced 
pkgver=1.0.0
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
source=("https://github.com/Luka287/ced/archive/refs/tags/1.0.0.tar.gz")
noextract=()
md5sums=()
validpgpkeys=()

build(){
	cd "$pkgname-$pkgver"
	
	cmake -DCMAKE_BUILD_TYPE=Debug -G Ninja "-DCMAKE_PREFIX_PATH=/path/to/Qt;/path/to/llvm" /path/to/qtcreator_sources

	cmake --build .
}

package(){
	cd "$pkgname-$pkgver"
	mkdir -p ${pkgdir}/opt/${pkgname}
	cp -rf * ${pkgdir}/opt/${pkgname}

	install -Dm644 LICENSE "${pkgdir}/usr/share/licenses/${pkgname}/LICENSE"
	install -Dm644 README.org "${pkgdir}/usr/share/doc/${pkgname}/README.org"
	
}

sha256sums=('252a45a28a80ddb1a0ba7811e94a1e75f8d716dd4db309f98b4b26624f072153')
