pkgname=tinymediamanager
pkgver=2.7.4
_commit=fceff9c
pkgrel=1
pkgdesc="An movies and tv shows organizer"
arch=('x86_64')
url="http://www.tinymediamanager.org/"
license=('APACHE')  
source=("http://release.tinymediamanager.org/dist/tmm_${pkgver}_${_commit}_linux.tar.gz" "tinyMediaManager.desktop")
depends=("java-runtime")
optdepends=("mediainfo")
md5sums=('b26fa4b01b984cbaed50417bd6d84528'
         '30e03d5ab8eaa74b7a3e9829b65cdd79')

package() {
   install -dm777 $pkgdir/opt/tinymediamanager 
   cp -r $srcdir/* $pkgdir/opt/tinymediamanager
   install -Dm644 $srcdir/tinyMediaManager.desktop $pkgdir/usr/share/applications/tinyMediaManager.desktop
   install -Dm644 $srcdir/tmm.png $pkgdir/usr/share/pixmaps/tinymediamanager.png
   install -dm755 $pkgdir/usr/bin
   ln -s  /opt/tinymediamanager/tinyMediaManager.sh $pkgdir/usr/bin/tinymediamanager 
   rm $pkgdir/opt/tinymediamanager/{tmm_${pkgver}_${_commit}_linux.tar.gz,tinyMediaManager.desktop}
    }   
