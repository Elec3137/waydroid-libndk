# Maintainer: Electria
# Created with the reference of: https://github.com/casualsnek/waydroid_script

pkgname=waydroid-libndk
pkgver=1
pkgrel=1
pkgdesc="libndk arm translation for Waydroid (android 11)"
arch=(x86_64)
url=
license=('GPL-3.0-or-later')
depends=('waydroid')
makedepends=()

source=('https://github.com/supremegamers/vendor_google_proprietary_ndk_translation-prebuilt/archive/9324a8914b649b885dad6f2bfd14a67e5d1520bf.zip')
md5sums=('c9572672d1045594448068079b34c350')

package() {
    _props=(
    "ro.product.cpu.abilist"
    "ro.product.cpu.abilist32"
    "ro.product.cpu.abilist64"
    "ro.dalvik.vm.native.bridge"
    "ro.enable.native.bridge.exec"
    "ro.vendor.enable.native.bridge.exec"
    "ro.vendor.enable.native.bridge.exec64"
    "ro.ndk_translation.version"
    "ro.dalvik.vm.isa.arm"
    "ro.dalvik.vm.isa.arm64")

    _values=(
    "x86_64,x86,armeabi-v7a,armeabi,arm64-v8a"
    "x86,armeabi-v7a,armeabi"
    "x86_64,arm64-v8a"
    "libndk_translation.so"
    "1"
    "1"
    "1"
    "0.2.3"
    "x86"
    "x86_64")

    for (( i=0; i<${#_props[*]}; i++ )); do
        sudo waydroid prop set ${_props[$i]} ${_values[$i]}
    done
}
