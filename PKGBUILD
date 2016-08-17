# Maintainer: Watcharapol Tadtiang <7aborigines7@gmail.com>
# Contributor: Ubuntu Developers <ubuntu-devel-discuss@lists.ubuntu.com>
pkgname=garmin-forerunner-tools
pkgver=0.10repacked.8
pkgrel=1
pkgdesc="Take a Break"
arch=('i686' 'x86_64')
license=('AGPL3')
depends=('sh' 'glibc' 'libusb')
url="https://launchpad.net/ubuntu/+source/garmin-forerunner-tools"

debianver=0.10repacked-8
source_i686=("https://launchpad.net/ubuntu/+source/garmin-forerunner-tools/${debianver}/+build/9419808/+files/garmin-forerunner-tools_${debianver}_i386.deb")
md5sums_i686=('48ebf5057d591f1b5110e55232cf61d2')

source_x86_64=("https://launchpad.net/ubuntu/+source/garmin-forerunner-tools/${debianver}/+build/9419805/+files/garmin-forerunner-tools_${debianver}_amd64.deb")
md5sums_x86_64=('a34772e52c3f9350f9171bce3c4aab18')

noextract=("${source[@]%%::*}")

prepare() {
	ar x ${srcdir}/*.deb
}

package() {
	tar axvf ${srcdir}/data.tar.xz
	cp -r ${srcdir}/lib ${pkgdir}/lib
	cp -r ${srcdir}/etc ${pkgdir}/etc
	cp -r ${srcdir}/usr ${pkgdir}/usr
}