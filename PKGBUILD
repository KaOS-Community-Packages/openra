pkgname=openra
pkgver=20170527
pkgrel=1
pkgdesc='A multiplayer re-envisioning of early RTS games by Westwood Studios.'
arch=('x86_64')
url='http://www.openra.net/'
license=('GPL3')
depends=("openal" "mono" "freetype2" "glibc" "alsa-lib" "libgl" "xdg-utils" "qarma" "sdl2" "lua")
source=("https://github.com/OpenRA/OpenRA/releases/download/release-${pkgver}/${pkgname}_release.${pkgver}_all.deb")
md5sums=('544c8023ba89f0d6b4f3f707ca4ba213')

package() {
    tar -xvf data.tar.gz -C $pkgdir
    rm -r $pkgdir/usr/share/doc
    ln -s /usr/lib/liblua.so.5.1 $pkgdir/usr/lib/liblua5.1.so.0
    find ${pkgdir}/usr/share/icons -type d -exec chmod 755 {} \;
    mv $pkgdir/usr/games $pkgdir/usr/bin
    }
