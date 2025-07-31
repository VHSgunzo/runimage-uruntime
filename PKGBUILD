# Maintainer: VHSgunzo <vhsgunzo.github.io>

pkgname='runimage-uruntime'
pkgver='0.4.3'
pkgrel='1'
pkgdesc='uruntime for RunImage container'
url='https://github.com/VHSgunzo/uruntime'
arch=('x86_64' 'aarch64')
license=('MIT')
options=(!strip)
provides=("uruntime=$pkgver-$pkgrel")
depends=('runimage-static')
source=("$url/releases/download/v$pkgver/uruntime-runimage-${CARCH}")
sha256sums=('SKIP')

package() {
  install -Dm755 "uruntime-runimage-${CARCH}" "${pkgdir}/var/RunDir/sharun/bin/uruntime"
  for bin in {dwarfs,dwarfsck,mkdwarfs,dwarfsextract,mksquashfs,unsquashfs,squashfuse}
    do ln -sfr "${pkgdir}/var/RunDir/sharun/bin/uruntime" "${pkgdir}/var/RunDir/sharun/bin/$bin"
  done
}
