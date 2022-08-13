# Maintainer: azasouth <azasouth(at)bigpond(dot)com>

_watch=('https://www.realvnc.com/en/connect/download/vnc/raspberrypi/' 'realvnc-vnc-server_(\d[\d.]*\d+)_ARM64\.deb')

pkgname=realvnc-vnc-server
pkgver=6.10.1
pkgrel=1
pkgdesc='VNC remote desktop server software by RealVNC'
arch=('aarch64')
url='https://www.realvnc.com/'
license=('custom')
depends=('libsm' 'libxtst' 'xorg-xauth' 'xterm' 'libxcrypt-compat')
optdepends=('cups: Printer support')
install='realvnc-vnc-server.install'
conflicts=('tightvnc' 'tigervnc' 'turbovnc')

source_aarch64=("https://www.realvnc.com/download/file/vnc.files/VNC-Server-${pkgver}-Linux-ARM64.deb")

sha256sums_aarch64=('aa327391628a8ca116db7654853d5692fd199b957041af9de40146dcd21bdb3a')

package() {
     
    bsdtar -xv -C "${pkgdir}" -f "${srcdir}/"data.tar.*
    mkdir -p "${pkgdir}/usr/share/licenses/${pkgname}"
    ln -s /usr/share/doc/${pkgname}/copyright "${pkgdir}/usr/share/licenses/${pkgname}/LICENSE"
    
}
