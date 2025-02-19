# Maintainer: Electria
# Created with the reference of: https://github.com/casualsnek/waydroid_script

pkgname=waydroid-libndk
pkgver=1
pkgrel=1
pkgdesc="libndk arm translation for Waydroid (android 11, overlayfs)"
arch=(x86_64)
url=https://github.com/Elec3137/waydroid-libndk
license=('GPL-3.0-or-later')
depends=('waydroid')
options=(!strip)

source=('https://github.com/supremegamers/vendor_google_proprietary_ndk_translation-prebuilt/archive/9324a8914b649b885dad6f2bfd14a67e5d1520bf.zip')
md5sums=('c9572672d1045594448068079b34c350')

install='.INSTALL'
package() {
    cd $srcdir/vendor_google_proprietary_ndk_translation-prebuilt-9324a8914b649b885dad6f2bfd14a67e5d1520bf/prebuilts

    install -d ${pkgdir}/var/lib/waydroid/overlay/system/
    cp -r ./* ${pkgdir}/var/lib/waydroid/overlay/system/
}
