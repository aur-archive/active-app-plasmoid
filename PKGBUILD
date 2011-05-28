# Contributor: Nuno Bento <ngpbento@gmail.com>

pkgname=active-app-plasmoid
pkgver=0.1.2
pkgrel=1
pkgdesc="A KDE plasmoid that just shows active application’s icon and name"
arch=('i686' 'x86_64')
url="http://kde-look.org/content/show.php/Active+Application?content=139686"
license=('LGPL')
depends=('kdebase-workspace')
makedepends=('cmake' 'automoc4' 'libxtst')
source=("http://kde-look.org/CONTENT/content-files/139686-active-app.tar.gz")
md5sums=('8f8949bb7768d442ae1c27264efeaf75')

build() {
  cd $srcdir
  mkdir build
  cd build
  cmake .. -DCMAKE_INSTALL_PREFIX=`kde4-config --prefix`
  make
}

package() {
  cd ${srcdir}/build
  make DESTDIR="$pkgdir" install
}
