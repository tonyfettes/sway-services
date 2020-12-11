# Maintainer: Antoine Damhet <antoine.damhet@lse.epita.fr>

_pkgname=sway-services
pkgname=${_pkgname}-git
pkgdesc="Collection of sway and friends systemd unit files"
pkgver=r28.dc7993a
pkgrel=1
arch=(any)
makedepends=('meson')
depends=('sway' 'swayidle' 'mako' 'kanshi' 'gammastep' 'waybar')
url="https://github.com/tonyfettes/sway-services"
source=("git+${url}.git")
license=('MIT')
md5sums=('SKIP')

pkgver() {
	cd "$srcdir/${_pkgname}"
	printf "r%s.%s" "$(git rev-list --count HEAD)" "$(git rev-parse --short HEAD)"
}

build() {
	arch-meson "$srcdir/${_pkgname}" build
}

package() {
	DESTDIR="${pkgdir}" ninja -C "${srcdir}/build" install
	install -D -m 0644 "${srcdir}/${_pkgname}/LICENSE" "${pkgdir}/usr/share/licenses/${pkgname}/LICENSE"
}
