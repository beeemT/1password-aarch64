pkgname=1password

_tarver=8.0.34
_tar="${pkgname}-${_tarver}.x64.tar.gz"
pkgver=${_tarver//-/_}
pkgrel=1
pkgdesc="Password manager and secure wallet"
arch=('x86_64')
url='https://1password.com'
license=('LicenseRef-1Password-Proprietary')
depends=('hicolor-icon-theme')
options=(!strip)
install="${pkgname}.install"
source=(https://downloads.1password.com/linux/tar/stable/x86_64/${_tar}{,.sig})
sha256sums=('b0f2e0e31a9d6ae3ce2a2ba97736876b13083bc14bdf6eef515bbf5d760ae156'
            '6f9e0001fd6c53f1eda4d5399a39c756c5d134aeeb686d0b563d12dad0300681'
)
validpgpkeys=('3FEF9748469ADBE15DA7CA80AC2D62742012EA22')

package() {
    # Go to source directory
    cd "${pkgname}-${_tarver}.x64"

    # Install icons
    resolutions=(32x32 64x64 256x256 512x512)
    for resolution in "${resolutions[@]}"
    do
        install -Dm0644 "resources/icons/hicolor/${resolution}/apps/${pkgname}.png" \
            "${pkgdir}/usr/share/icons/hicolor/${resolution}/apps/${pkgname}.png"
    done
    # Install desktop file
    install -Dm0644 resources/${pkgname}.desktop -t "${pkgdir}"/usr/share/applications/
    # Install system unlock PolKit policy file
    install -Dm0644 com.1password.1Password.policy -t "${pkgdir}"/usr/share/polkit-1/actions/

    # Install examples
    install -Dm0644 resources/custom_allowed_browsers -t "${pkgdir}"/usr/share/doc/${pkgname}/examples/

    # Move package contents to /opt/1Password
    cd "${srcdir}"
    install -dm0755 "${pkgdir}"/opt
    mv "${pkgname}-${_tarver}.x64" "${pkgdir}/opt/1Password"

    # Symlink /usr/bin executable to opt
    install -dm0755 "${pkgdir}"/usr/bin
    ln -s /opt/1Password/${pkgname} "${pkgdir}"/usr/bin/${pkgname}
}
