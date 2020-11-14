pkgname=idea
pkgver=2020.2.3
_build=202.7660.26
pkgrel=1
pkgdesc="The Java IDE for Professional Developers by JetBrains"
arch=('x86_64')
options=('!strip')
url="https://www.jetbrains.com/idea/"
license=('custom: https://www.jetbrains.com/legal/agreements/user.html')
install='idea.install'
source=("https://download.jetbrains.com/idea/ideaIU-${pkgver}.tar.gz"
        "${pkgname}.desktop")
sha512sums=('7eedd47f9e4de510d2f7e9485655721585d892aad35888b4d71da2506f2175065bc3c1adf87dc2bd3f1d520a93abf098d0b65b11dce3f9638f0b3420b905ad4e'
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
