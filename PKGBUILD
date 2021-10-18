# Maintainer: Jonas Schwartz
pkgname=galaxybudsclient
_pkgname=GalaxyBudsClient
pkgver=4.4.1
pkgrel=1
pkgdesc="Galaxy Buds Client for Linux"
arch=('x86_64'
      'armv7h'
      'aarch64')
url="https://github.com/ThePBone/GalaxyBudsClient"
license=('GPL3')
depends=()
makedepends=('git' 'wget')
provides=("${pkgname}")
conflicts=("${pkgname}")
options=("!strip")
source=("${pkgname}.desktop" "icon_white.png")
source_x86_64=("https://github.com/ThePBone/GalaxyBudsClient/releases/download/${pkgver}/${_pkgname}_Linux_64Bit_Portable.bin")
sha256sums=('bc638a601547b4dd3adf519ddf8cc962205ac2656b1a10a1a5b3e889e8754a1a'
            '04b551470a2e0ccd99b266d313265321113886f5808b872bf928a97442bf930a')
sha256sums_x86_64=('eef881b49f5bceea153870c7b82633e2a5eeec82ddc6949883a7c9ed3e074ae4')

package() {
	install -Dm755 ${_pkgname}_Linux_64Bit_Portable.bin "$pkgdir/usr/bin/galaxybudsclient"
	install -Dm644 "$srcdir/${pkgname}.desktop" -t "$pkgdir/usr/share/applications"
	install -Dm644 "$srcdir/icon_white.png" "$pkgdir/usr/share/pixmaps/galaxybudsclient.png"
}
