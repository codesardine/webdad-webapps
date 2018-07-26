# Maintainer: Vitor Lopes <vmnlop@gmail.com>

_pkgname=webdad-webapps
pkgname="$_pkgname-git"
pkgver=r4.93b4371
pkgrel=1
pkgdesc="JAK Web Application wrappers for Manjaro Forum/Wiki and Arch Wiki"
arch=('any')
url="https://github.com/codesardine/webdad-webapps"
license=('GPL')
makedepends=('git')
source=("git+$url.git")
sha256sums=('SKIP')
conflicts=('webdad-webapps')
provides=('webdad-webapps')
depends=('python-jade-application-kit')

pkgver() {
    cd "$_pkgname"
    (
        printf "r%s.%s" "$(git rev-list --count HEAD)" "$(git rev-parse --short HEAD)"
    )
}

package(){
	cd "$_pkgname"
	cp -r $srcdir/$_pkgname/usr $pkgdir/
        chmod 644 $pkgdir/usr/share/applications/Manjaro-Forum.desktop
        chmod 644 $pkgdir/usr/share/applications/Manjaro-Wiki.desktop
        chmod 644 $pkgdir/usr/share/applications/Arch-Wiki.desktop
        chmod a+x $pkgdir/usr/share/webapps/manjaro/forum/manjaro-forum
        chmod a+x $pkgdir/usr/share/webapps/manjaro/wiki/manjaro-wiki
        chmod a+x $pkgdir/usr/share/webapps/manjaro/wiki/manjaro-wiki
}
