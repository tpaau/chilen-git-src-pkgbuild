# Maintainer: tpaau <tpaau-17db@tutamail.com>
pkgname=chilen-git-src
pkgver=git
pkgrel=1
pkgdesc="Fully offline, blazingly fast music player for your library"
arch=(any)
url="https://github.com/tpaau/chilen"
license=('GPL-3.0-or-later')
depends=(wayland libxkbcommon)
makedepends=(git cargo alsa-lib)
provides=("chilen-git=$pkgver")
source=(git+https://github.com/tpaau/chilen.git)
b2sums=(SKIP)

pkgver() {
	cd "${srcdir}/chilen"
	printf 'r%s.%s' "$(git rev-list --count HEAD)" "$(git rev-parse --short HEAD)"
}

build() {
	cd "$srcdir/chilen"
	# TODO: The git version can be considered a development build so the `dev-opts` feature is enabled
	cargo build --release --features mpris --features dev-opts
}

package() {
	cd "$srcdir/chilen"
	install -Dm755 target/release/chilen "${pkgdir}/usr/bin/chilen-git"
	install -Dm644 LICENSE "${pkgdir}/usr/share/licenses/${pkgname}/LICENSE"
}
