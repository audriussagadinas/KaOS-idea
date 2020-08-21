
pkgname=idea
pkgver=2020.2
_build=202.6397.94
pkgrel=1
pkgdesc="The Java IDE for Professional Developers by JetBrains"
arch=('x86_64')
url="https://www.jetbrains.com/idea/"
license=('custom: https://www.jetbrains.com/legal/agreements/user.html')
install='idea.install'
source=("https://download.jetbrains.com/idea/ideaIU-${pkgver}.tar.gz"
        "${pkgname}.desktop")
md5sums=('20de0107ec38b37bca0b7c2d361cebce'
         '2b0f3337e0ddb80722d61249707d0774')

package() {
    install -d -m 755 ${pkgdir}/opt/
    install -d -m 755 ${pkgdir}/usr/bin/
    install -d -m 755 ${pkgdir}/usr/share/applications/
    install -d -m 755 ${pkgdir}/usr/share/icons/hicolor/128x128/apps/

    cd ${srcdir}
    cp -a idea-IU-${_build} ${pkgdir}/opt/${pkgname}

    ln -s /opt/${pkgname}/bin/${pkgname}.sh ${pkgdir}/usr/bin/${pkgname}
    install -D -m 644 ${srcdir}/${pkgname}.desktop ${pkgdir}/usr/share/applications/
    install -D -m 644 ${pkgdir}/opt/${pkgname}/bin/${pkgname}.png ${pkgdir}/usr/share/icons/hicolor/128x128/apps/${pkgname}.png
}
