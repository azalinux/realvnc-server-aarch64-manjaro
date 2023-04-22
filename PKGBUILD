# Maintainer: azasouth <azasouth(at)bigpond(dot)com>

_watch=('https://downloads.realvnc.com/en/connect/download/vnc/raspberrypi/' 'realvnc-vnc-server_(\d[\d.]*\d+)_ARM64\.deb')

pkgname=realvnc-vnc-server
pkgver=7.1.0
pkgrel=1
pkgdesc='VNC remote desktop server software by RealVNC'
arch=('aarch64')
url='https://www.realvnc.com/'
license=('custom')
depends=('libsm' 'libxtst' 'xorg-xauth' 'xterm' 'libxcrypt-compat')
optdepends=('cups: Printer support')
install='realvnc-vnc-server.install'
conflicts=('tightvnc' 'tigervnc' 'turbovnc')

source_aarch64=("https://downloads.realvnc.com/download/file/vnc.files/VNC-Server-${pkgver}-Linux-ARM64.deb")

sha256sums_aarch64=('687c87f467875e820d74bb725ecd534866a13fe74220e0973bf68de7eea85677')

package() {
     
    bsdtar -xv -C "${pkgdir}" -f "${srcdir}/"data.tar.*
    mkdir -p "${pkgdir}/usr/share/licenses/${pkgname}"
    ln -s /usr/share/doc/${pkgname}/copyright "${pkgdir}/usr/share/licenses/${pkgname}/LICENSE"
    sudo mv /usr/bin/vncserver /usr/bin/vncserver.bak
}
