pkgname=schenker-oled-brightness
pkgrel=1
pkgver=r14.805ebb1
pkgdesc="Tool for adjusting the brightness of schenker laptop with AMOLED screen"
arch=("any")
url="https://github.com/pop-os/system76-oled"
license=('GPL')
groups=()
depends=(dbus)
makedepends=(rust)
install=
source=(git+$url "$pkgname.patch")
md5sums=("SKIP" "4149d111b2930a32e6b9ea504569b334")
validpgpkeys=()

pkgver() {
    cd "$srcdir/system76-oled"
    printf 'r%s.%s' "$(git rev-list --count HEAD)" "$(git rev-parse --short HEAD)"
}

prepare() {
    cd system76-oled
	patch -p1 -i "$srcdir/$pkgname.patch"
}

build() {
	cd "system76-oled"
	make
}

package() {
	cd "system76-oled"
	make DESTDIR="$pkgdir/" install
}
