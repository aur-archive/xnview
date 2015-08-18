# Contributor: Olivier Duclos <olivier.duclos@gmail.com>

pkgname=xnview
pkgver=1.70
pkgrel=5
pkgdesc="An efficient image viewer, browser and converter."
arch=('i686' 'x86_64')
url="http://www.xnview.com"
license=('custom:xnview')
[ "$CARCH" = "i686" ]   && depends=('gcc-libs' 'libxp' 'libxt')
[ "$CARCH" = "x86_64" ] && depends=('lib32-gcc-libs' 'lib32-libxp' 'lib32-libxt')
source=(http://download.xnview.com/XnView-x86-unknown-linux2.x-static-fc4.tgz)
md5sums=('b5ab466eb572a6ea429a9c579644e582')

build() {
   install -d $startdir/pkg/usr/bin
   install -d $startdir/pkg/usr/share/doc/$pkgname
   install -d $startdir/pkg/usr/share/man/man1
   cd $srcdir/XnView-1.70-x86-unknown-linux2.x-static-fc4
   install -m 755 bin/* $startdir/pkg/usr/bin
   install -m 644 man/*.1 $startdir/pkg/usr/share/man/man1
   install -m 644 *.txt $startdir/pkg/usr/share/doc/$pkgname
   install -m 644 -D app-defaults/XnView.ad $startdir/pkg/usr/lib/X11/app-defaults/XnView
   install -m 644 -D ReadMe.txt $startdir/pkg/usr/share/licenses/$pkgname/license.txt
}
