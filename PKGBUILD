# Maintainer: Flow

pkgname=swift-explorer
pkgver=1.0.7
pkgrel=1
pkgdesc="User-friendly tool to manage files in an OpenStack Storage system (SWIFT)"
license=('apachev2')
depends=("jre")
noextract=('SwiftExplorer-${pkgver}-jar-with-dependencies.jar')
conflicts=()
url="http://www.619.io/swift-explorer"
arch=(any)
source=("SwiftExplorer-${pkgver}-jar-with-dependencies.jar::https://docs.google.com/uc?authuser=0&id=0BzGvcxyAVysRSGV4cnR2WW83U00&export=download"
        "swift-explorer.sh"
        "swift-explorer.png"
        "swift-explorer.desktop"
        "LICENSE")
md5sums=('40ddf62b8b46d0992ea6250354d19380'
         '0f2a52319a239eb70d0849b0223aad3b'
         '2a8d702d3c76a5c627dacd4534d5581d'
         'd64f444c2a263ec4db1a584b88b117ef'
         'd2794c0df5b907fdace235a619d80314')

package() {
    cd "$srcdir"
    install -D -m755 "${srcdir}/${pkgname}.sh"                                         "${pkgdir}/usr/bin/${pkgname}"
    install -D -m644 "${srcdir}/SwiftExplorer-${pkgver}-jar-with-dependencies.jar"     "${pkgdir}/usr/share/${pkgname}/${pkgname}.jar"

    # Desktop launcher with icon
    install -D -m644 "${srcdir}/${pkgname}.desktop" "${pkgdir}/usr/share/applications/${pkgname}.desktop"
    install -D -m644 "${srcdir}/${pkgname}.png"     "${pkgdir}/usr/share/pixmaps/${pkgname}.png"

    # License
    install -D -m644 "${srcdir}/LICENSE"           "${pkgdir}/usr/share/licenses/${pkgname}/LICENSE"
}
