# Maintainer: azasouth <azasouth(at)bigpond(dot)com>

_watch=('https://downloads.realvnc.com/en/connect/download/vnc/raspberrypi/' 'realvnc-vnc-server_(\d[\d.]*\d+)_ARM64\.deb')

pkgname=realvnc-vnc-server
pkgver=7.5.0
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

sha256sums_aarch64=('fa4b96fc6c00bf068bc164f22619d64a0187c23ff0724730bcc3e8f18bc64263')

package() {
     
    bsdtar -xv -C "${pkgdir}" -f "${srcdir}/"data.tar.*
    mkdir -p "${pkgdir}/usr/share/licenses/${pkgname}"
    ln -s /usr/share/doc/${pkgname}/copyright "${pkgdir}/usr/share/licenses/${pkgname}/LICENSE"
    if [ -e "/usr/bin/vncserver" ]; then
    echo "File /usr/bin/vncserver exists. Renaming to /usr/bin/vncserver.bak"
    sudo mv /usr/bin/vncserver /usr/bin/vncserver.bak
    else
    echo "File /usr/bin/vncserver does not exist - continuing with installation :-)."
  fi

}
