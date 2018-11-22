pkgname=tinymediamanager
pkgver=2.9.13
_commit=5cfe5d1
pkgrel=1
pkgdesc="An movies and tv shows organizer"
arch=('x86_64')
url="http://www.tinymediamanager.org/"
license=('APACHE')  
source=("http://release.tinymediamanager.org/dist/tmm_${pkgver}_${_commit}_linux.tar.gz" "tinyMediaManager.desktop")
depends=('java-runtime' 'mediainfolib')
sha1sums=('b1c763c0e530fbebde1541c13da5b9d448305247'
          '351046a17408fa7cc61f84554f5109268a61e2ae')

package() {
   install -dm777 $pkgdir/opt/tinymediamanager 
   cp -r $srcdir/* $pkgdir/opt/tinymediamanager
   install -Dm644 $srcdir/tinyMediaManager.desktop $pkgdir/usr/share/applications/tinyMediaManager.desktop
   install -Dm644 $srcdir/tmm.png $pkgdir/usr/share/pixmaps/tinymediamanager.png
   install -dm755 $pkgdir/usr/bin
   ln -s  /opt/tinymediamanager/tinyMediaManager.sh $pkgdir/usr/bin/tinymediamanager 
   rm $pkgdir/opt/tinymediamanager/{tmm_${pkgver}_${_commit}_linux.tar.gz,tinyMediaManager.desktop}
    }
