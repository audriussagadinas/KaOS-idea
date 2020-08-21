pkgname=idea
pkgver=2020.2
_build=202.6397.94
pkgrel=1
pkgdesc="The Java IDE for Professional Developers by JetBrains"
arch=('x86_64')
options=('!strip')
url="https://www.jetbrains.com/idea/"
license=('custom: https://www.jetbrains.com/legal/agreements/user.html')
install='idea.install'
source=("https://download.jetbrains.com/idea/ideaIU-${pkgver}.tar.gz"
        "${pkgname}.desktop")
sha512sums=('89cf641c2f8b73215cc9ab44720683507136fa82636a56e4e18308ec31ef2452d1dfa6da0849f75a55badd8e28291a0411c3c464d8593fb80ac675db6c217282'
            '9e7daafedc1ed48508ebf8b405dadc22659052f9e55a6931fe2f3d90e1ccd571ec8b37ba387ae1317036cd4875005ae85d247e18153c4678354ab2af5f31a762')

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
