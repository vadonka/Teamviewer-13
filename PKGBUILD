# Maintainer: liberodark

pkgname=teamviewer13
pkgdesc='All-In-One Software for Remote Support and Online Meetings'
pkgver='13.2.75536'
pkgrel='2'
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

source_x86_64=("https://download.teamviewer.com/download/linux/version_${pkgver%%.*}x/teamviewer-host_amd64.deb")
source=($pkgname.desktop
        $pkgname.png)

sha512sums=('0145af7977bb673957d7066ae9c9faf3791b854a3f689eef9f31e144ab2f19b4c02e2599ab6acf3d0c1b08a5f15b34522640ed1d818791c6a8a3251db1e796f9'
            '1222cbb98505294adbbf1bfb59abcd0e645aa3eeae50f658a32355ed3b3ee087cea64a31163df5ca18119aca613526fc80e7f1f50d0c77ceda88d86e6811447c')
sha512sums_x86_64=('33610874418c37c61d4847ce39ed9d83ff3a49b57c7ca12fa2f8a6eefd3e21bcf4e40175d00b57c48472b50d69b2a2af50d776b924b85bc1b2b058cf74e377d4')


package() {
  cd $srcdir
  tar xvf data.tar.xz
  cp -r opt $pkgdir
  install -vDm644 $srcdir/$pkgname.desktop $pkgdir/usr/share/applications/$pkgname.desktop
  install -vDm644 $srcdir/$pkgname.png $pkgdir/usr/share/pixmaps/$pkgname.png
}
