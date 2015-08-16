
pkgname=magicseteditor-mtg-base
pkgver=20140808
pkgrel=2
pkgdesc="Magic Set Editor shared game files for Magic: The Gathering"
arch=(any)
url="http://msetemps.sourceforge.net/phpBB3/viewtopic.php?t=144"
license=('freeware')
depends=('magicseteditor')
conflicts=("mse-mtg")
source=("http://downloads.sourceforge.net/msetemps/Magic - Printed Modern Styles.mse-installer")
md5sums=('3c47596e24226707942d4f3f736f916c')

package() {
  install -d $pkgdir/usr/share/magicseteditor/data
  cd $srcdir
  find magic.mse-game -name '*.png' -type f -exec mogrify {} \;
  cp -r magic.mse-game $pkgdir/usr/share/magicseteditor/data
  find magic-{blends,default-image,embossedletters,identity-new,mana-large,mana-small,watermarks}.* -name '*.png' -type f -exec mogrify {} \;
  cp -r magic-{blends,default-image,embossedletters,identity-new,mana-large,mana-small,watermarks}.* $pkgdir/usr/share/magicseteditor/data
  chmod -R 755 $pkgdir/usr/share/magicseteditor/data/*
}
