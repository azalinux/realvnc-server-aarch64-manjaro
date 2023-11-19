# Maintainer: azasouth <azasouth(at)bigpond(dot)com>

_watch=('https://downloads.realvnc.com/en/connect/download/vnc/raspberrypi/' 'realvnc-vnc-server_(\d[\d.]*\d+)_ARM64\.deb')

pkgname=realvnc-vnc-server
pkgver=7.8.0
pkgrel=2
pkgdesc='VNC remote desktop server software by RealVNC'
arch=('aarch64')
url='https://www.realvnc.com/'
license=('custom')
depends=('libsm' 'libxtst' 'xorg-xauth' 'xterm' 'libxcrypt-compat')
optdepends=('cups: Printer support')
install='realvnc-vnc-server.install'
conflicts=('tightvnc' 'tigervnc' 'turbovnc')

source_aarch64=("https://downloads.realvnc.com/download/file/vnc.files/VNC-Server-${pkgver}-Linux-ARM64.deb" "https://github.com/azalinux/realvnc-server-aarch64-fedora/raw/main/pifirmware_libs.tar.gz")

sha256sums_aarch64=('b2f88cc9e695bf49482bdc05e529769afaf326bcded149f4d7d2182170e36136' '224709560792f4347ad8e3700dac72fd341582081d2b7c26d9a8e33d583af703')

build() {
  # Extract the source files
  if [ ! -d "/opt/vc" ]; then
  sudo mkdir -p /opt/vc
  sudo tar xvf pifirmware_libs.tar.gz -C /opt/vc/
  
  else
    echo "/opt/vc exists, moving on.."
 fi   
  if [ ! -f "/opt/vc/lib/libvcos.so" ] || [ ! -f "/usr/lib/libvcos.so.0" ] || [ ! -f "/opt/vc/lib/libvchiq_arm.so" ] || [ ! -f "/usr/lib/libvchiq_arm.so.0" ] || [ ! -f "/opt/vc/lib/libbcm_host.so" ] || [ ! -f "/usr/lib/libbcm_host.so.0" ]; then
  sudo ln -s /opt/vc/lib/libvcos.so /usr/lib/libvcos.so.0
  sudo ln -s /opt/vc/lib/libvchiq_arm.so /usr/lib/libvchiq_arm.so.0
  sudo ln -s /opt/vc/lib/libbcm_host.so /usr/lib/libbcm_host.so.0
else
  echo "libvcos.so, libvchiq_arm, libbcm_host sym links already exists so moving on..."
fi
}

package() {
    
    
    bsdtar -xv -C "${pkgdir}" -f "${srcdir}/"data.tar.*
    mkdir -p "${pkgdir}/usr/share/licenses/${pkgname}"
    ln -s /usr/share/doc/${pkgname}/copyright "${pkgdir}/usr/share/licenses/${pkgname}/LICENSE"

}
