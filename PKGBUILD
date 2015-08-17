# Maintainer: eruditorum
pkgname=powerconf
pkgdesc="Udev-driven user-configurable power management system for Linux"
license=('none')
url="https://bbs.archlinux.org/viewtopic.php?pid=1200758"
pkgrel=3
pkgver=1
arch=('any')
depends=('sh')
optdepends=('iw: WLAN power control' 'ethtool: LAN power control' 'hdparm: HDD power control')
install='powerconf.install'
source=("http://mp-lab.narod.ru/files/powerconf.tar.xz")
sha256sums=('abdfe1188a0584166ac6caa632caeea4b0e2ea4e40b9ad14fdcc0ef13b158e3d')
sha384sums=('50315fa798bc5ba3fbad23471f7cab92844c6e901d1ed7ddcc2088bbef28d4b9118a3eb53fa7b6878fc992208006fc5a')
sha512sums=('fcaf8112cfceeef2df71968bbb7e552ef71fdff273b51b3ad63e1f96c0f6a24d73bf4b9ac3e3ccf6b9fc18030973b5e9c88932b72c619dc0f82f3c851e4e3dd9')
backup=('etc/udev/rules.d/powerconf.rules' 'etc/powerconf/battery' 'etc/powerconf/resume' 'etc/powerconf/offline' 'etc/powerconf/online')

package() {
  install -Dm644 "$srcdir/powerconf.rules" "$pkgdir/etc/udev/rules.d/powerconf.rules"
  install -Dm744 "$srcdir/powerconf/battery" "$pkgdir/etc/powerconf/battery"
  install -Dm744 "$srcdir/powerconf/resume" "$pkgdir/etc/powerconf/resume"
  install -Dm744 "$srcdir/powerconf/offline" "$pkgdir/etc/powerconf/offline"
  install -Dm744 "$srcdir/powerconf/online" "$pkgdir/etc/powerconf/online"
}