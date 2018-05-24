pkgname=openra
pkgver=20180307
pkgrel=1
pkgdesc='A multiplayer re-envisioning of early RTS games by Westwood Studios.'
arch=('x86_64')
url='http://www.openra.net/'
license=('GPL3')
depends=("openal" "mono" "freetype2" "glibc" "alsa-lib" "libgl" "xdg-utils" "qarma" "sdl2" "lua")
source=("https://github.com/OpenRA/OpenRA/releases/download/release-${pkgver}/${pkgname}_release.${pkgver}_all.deb")
md5sums=('0ac7b0ea5214903ff59c3d887b38fd0e')

package() {
    tar -xvf data.tar.xz -C $pkgdir
    rm -r $pkgdir/usr/share/doc
    ln -s /usr/lib/liblua.so.5.1 $pkgdir/usr/lib/liblua5.1.so.0
    find ${pkgdir}/usr/share/icons -type d -exec chmod 755 {} \;
    mv $pkgdir/usr/games $pkgdir/usr/bin
    }
