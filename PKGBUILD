_mode=cross
pkgname=mkbootimg-git
pkgver=r254.ba2684e
pkgrel=2
_arches=specific
arch=(aarch64)
license=(
    Apache
    MIT
)
url=https://android.googlesource.com/platform/system/tools/mkbootimg
provides=(mkbootimg)
depends=(
    python
)
_commit=ba2684e38651df5784be5eaa8260baade15a2c5d
source=("git+$url#commit=$_commit")
sha256sums=(SKIP)

pkgver() {
    cd "$srcdir"/mkbootimg
    printf "r%s.%s" "$(git rev-list --count HEAD)" "$(git rev-parse --short HEAD)"
}

package() {
    install -m755 -d "$pkgdir"/usr/bin
    install -Dm 755 mkbootimg/mkbootimg.py "$pkgdir"/usr/bin/mkbootimg
    install -Dm 755 mkbootimg/unpack_bootimg.py "$pkgdir"/usr/bin/unpack_bootimg
}
