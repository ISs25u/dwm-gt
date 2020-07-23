_pkgname=dwm
pkgname=dwm-gt-git
pkgver=6.2
pkgrel=1
pkgdesc="GT's customized version of dwm"
arch=('any')
url="https://github.com/ISs25u/dwm-gt"
license=('MIT')
depends=('libx11' 'libxinerama' 'freetype2')
makedepends=('git')
optdepends=('libxft-bgra: for emojis in statusbar')
provides=($_pkgname)
conflicts=($_pkgname)
source=("git+$url.git")
md5sums=('SKIP')

pkgver() {
	cd "${_pkgname}-gt"
	printf "%s" "$(git describe --long --tags | sed 's/\([^-]*-\)g/r\1/;s/-/./g')"
}

build() {
	cd "${_pkgname}-gt"
	make X11INC=/usr/include/X11/ X11LIB=/usr/lib/X11 FREETYPEINC=/usr/include/freetype2
}

package() {
	cd "${_pkgname}-gt"
	make DESTDIR="${pkgdir}" PREFIX=/usr install
	install -Dm 644 LICENSE "${pkgdir}/usr/share/${pkgname%-git}/LICENSE"
}

