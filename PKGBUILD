# Maintainer: azasouth <azasouth(at)bigpond(dot)com>

_watch=('https://downloads.realvnc.com/en/connect/download/vnc/raspberrypi/' 'realvnc-vnc-server_(\d[\d.]*\d+)_ARM64\.deb')

pkgname=realvnc-vnc-server
pkgver=7.11.0
pkgrel=1
pkgdesc='VNC remote desktop server software by RealVNC'
arch=('aarch64')
url='https://www.realvnc.com/'
license=('custom')
depends=('libsm' 'libxtst' 'xorg-xauth' 'xterm' 'libxcrypt-compat')
optdepends=('cups: Printer support')
install='realvnc-vnc-server.install'
conflicts=('tightvnc' 'tigervnc' 'turbovnc')

source_aarch64=("https://downloads.realvnc.com/download/file/vnc.files/VNC-Server-${pkgver}-Linux-ARM64.deb" "https://github.com/azalinux/realvnc-server-aarch64-fedora/raw/main/pifirmware_libs.tar.gz")

sha256sums_aarch64=('1715119b1550ff46355c585306bf16783ea68443d7d9b5967735fcf85cf5d570' '224709560792f4347ad8e3700dac72fd341582081d2b7c26d9a8e33d583af703')


package() {
    
    
    bsdtar -xv -C "${pkgdir}" -f "${srcdir}/"data.tar.*
    mkdir -p "${pkgdir}/usr/share/licenses/${pkgname}"
    ln -s /usr/share/doc/${pkgname}/copyright "${pkgdir}/usr/share/licenses/${pkgname}/LICENSE"

}
