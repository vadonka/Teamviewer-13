# Maintainer: liberodark

pkgname=teamviewer13
pkgver=13.0.5494
pkgrel=2
pkgdesc='All-In-One Software for Remote Support and Online Meetings'
arch=('x86_64')
url='http://www.teamviewer.com'
license=('custom')
options=('!strip')
provides=('teamviewer')
conflicts=('teamviewer' 'teamviewer-beta' 'teamviewer12' 'teamviewer11' 'teamviewer10' 'teamviewer9' 'teamviewer8')
depends=('hicolor-icon-theme'
         'qt5-quickcontrols'
         'qt5-webkit'
         'qt5-x11extras')

source_x86_64=("https://download.teamviewer.com/download/version_${pkgver%%.*}x/teamviewer_${pkgver}_amd64.deb")
source=($pkgname.desktop
        $pkgname.png)

sha512sums=('0145af7977bb673957d7066ae9c9faf3791b854a3f689eef9f31e144ab2f19b4c02e2599ab6acf3d0c1b08a5f15b34522640ed1d818791c6a8a3251db1e796f9'
         '1222cbb98505294adbbf1bfb59abcd0e645aa3eeae50f658a32355ed3b3ee087cea64a31163df5ca18119aca613526fc80e7f1f50d0c77ceda88d86e6811447c')

sha512sums_x86_64=('00b70833c59d81d4f6124f0c5a98e69b52197eb3697066c1440a4611857cbec9d00d9644d2a1281c606b248a6c44fa70962ccbb50464a85abb757f985683a1df')

package() {
  cd $srcdir
  tar xvf data.tar.xz
  cp -r opt $pkgdir
  install -vDm644 $srcdir/$pkgname.desktop $pkgdir/usr/share/applications/$pkgname.desktop
  install -vDm644 $srcdir/$pkgname.png $pkgdir/usr/share/pixmaps/$pkgname.png
}
