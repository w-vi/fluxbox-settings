_pkgbase=desktop-settings

pkgname=fluxbox-desktop-settings
pkgver=20171229
pkgrel=1
pkgdesc='Manjaro Linux fluxbox settings'
arch=('any')
url="https://github.com/w-vi/fluxbox-settings"
license=('GPL')
provides=('fluxbox-desktop-settings')
depends=('manjaro-base-skel'
        'cantarell-fonts'
        'fbmenugen'
        'fluxbox-theme-manjaro'
        'fluxbox-wallpapers'
        'menda-themes-dark'
        'numix-reborn-icon-themes'
        'oblogout-manjaro'
        'xcursor-menda'
        'xfce-theme-greenbird')
makedepends=('git')
conflicts=('manjaro-desktop-settings'
           'fluxbox-desktop-settings')
source=("git+$url.git")
sha256sums=('SKIP')

_inst_dir(){
    if [[ -d $srcdir/$_pkgbase/$1/skel ]]; then
        install -d $pkgdir/etc
        cp -r $srcdir/$_pkgbase/$1/skel $pkgdir/etc
    fi

    if [[ -d $srcdir/$_pkgbase/$1/scripts ]]; then
        install -d $pkgdir/usr/bin
        cp $srcdir/$_pkgbase/$1/scripts/* $pkgdir/usr/bin
    fi
}

pkgver() {
    date +%Y%m%d
}

package() {
    _inst_dir 'community/fluxbox'
}
