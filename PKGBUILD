# Maintainer: azasouth <azasouth(at)bigpond(dot)com>

_watch=('https://archive.raspberrypi.org/debian/pool/main/r/realvnc-vnc/' 'realvnc-vnc-server_(\d[\d.]*\d+)_arm64\.deb')

pkgname=realvnc-vnc-server
pkgver=6.7.2.43081
pkgrel=1
pkgdesc='VNC remote desktop server software by RealVNC'
arch=('aarch64')
url='https://www.realvnc.com/'
license=('custom')
depends=('libsm' 'libxtst' 'xorg-xauth')
optdepends=('cups: Printer support')
install='realvnc-vnc-server.install'
conflicts=('tightvnc' 'tigervnc' 'turbovnc')

source_aarch64=("http://archive.raspberrypi.org/debian/pool/main/r/realvnc-vnc/realvnc-vnc-server_${pkgver}_arm64.deb")

md5sums_aarch64=('7e6d0bea799a71c75c72b82073e5f3e6')

package() {
     
    bsdtar -xv -C "${pkgdir}" -f "${srcdir}/"data.tar.*
    mkdir -p "${pkgdir}/usr/share/licenses/${pkgname}"
    ln -s /usr/share/doc/${pkgname}/copyright "${pkgdir}/usr/share/licenses/${pkgname}/LICENSE"
    
}
