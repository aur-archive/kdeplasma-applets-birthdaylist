pkgname=kdeplasma-applets-birthdaylist
pkgver=1.0.2
pkgrel=1
pkgdesc="Shows a sorted list of coming birthdays, namedays and anniversaries from the selected Akonadi collection"
arch=('i686' 'x86_64')
url="http://kde-look.org/content/show.php/Birthday+List?content=121134"
license=('GPL')
depends=('kdebase-workspace')
makedepends=('cmake' 'automoc4' 'boost')
conflicts=('plasmoid-birthdaylist')
replaces=('plasmoid-birthdaylist')
source=("http://kde-look.org/CONTENT/content-files/121134-birthdaylist-$pkgver-$pkgrel.tar.gz")
md5sums=('e3085418cac723ed281c8bfeee9c7e4e')

build() {
  mkdir build
  cd build
  cmake ../birthdaylist-$pkgver-$pkgrel \
    -DCMAKE_INSTALL_PREFIX=`kde4-config --prefix` \
    -DCMAKE_BUILD_TYPE=Release
  make
}

package() {
  cd build
  make DESTDIR="${pkgdir}" install
}
