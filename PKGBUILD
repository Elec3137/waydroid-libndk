# Maintainer: Electria
# Created with the reference of: https://github.com/casualsnek/waydroid_script

pkgname=waydroid-libndk
pkgver=1
pkgrel=1
pkgdesc="libndk arm translation for Waydroid (android 11, overlayfs)"
arch=(x86_64)
url=
license=('GPL-3.0-or-later')
depends=('waydroid')
makedepends=()

source=('https://github.com/supremegamers/vendor_google_proprietary_ndk_translation-prebuilt/archive/9324a8914b649b885dad6f2bfd14a67e5d1520bf.zip')
md5sums=('c9572672d1045594448068079b34c350')

install='.install'
package() {
    cd $srcdir/vendor_google_proprietary_ndk_translation-prebuilt-9324a8914b649b885dad6f2bfd14a67e5d1520bf/prebuilts

    install -d ${pkgdir}/var/lib/waydroid/overlay/system/bin/
    cp -r bin/arm ${pkgdir}/var/lib/waydroid/overlay/system/bin/
    cp -r bin/arm64 ${pkgdir}/var/lib/waydroid/overlay/system/bin/
    cp bin/ndk_translation_program_runner_binfmt_misc ${pkgdir}/var/lib/waydroid/overlay/system/bin/
    cp bin/ndk_translation_program_runner_binfmt_misc_arm64 ${pkgdir}/var/lib/waydroid/overlay/system/bin/

    install -d ${pkgdir}/var/lib/waydroid/overlay/system/etc/
    cp -r etc/binfmt_misc ${pkgdir}/var/lib/waydroid/overlay/system/etc/
    cp etc/ld.config.arm.txt ${pkgdir}/var/lib/waydroid/overlay/system/etc/
    cp etc/ld.config.arm64.txt ${pkgdir}/var/lib/waydroid/overlay/system/etc/
    cp etc/init/ndk_translation.rc ${pkgdir}/var/lib/waydroid/overlay/system/etc/

    install -d ${pkgdir}/var/lib/waydroid/overlay/system/lib/
    cp -r lib/arm ${pkgdir}/var/lib/waydroid/overlay/system/lib/
    cp lib/libndk* ${pkgdir}/var/lib/waydroid/overlay/system/lib/

    install -d ${pkgdir}/var/lib/waydroid/overlay/system/lib64/
    cp -r lib64/arm64 ${pkgdir}/var/lib/waydroid/overlay/system/lib64/
    cp lib64/libndk* ${pkgdir}/var/lib/waydroid/overlay/system/lib64/

}
