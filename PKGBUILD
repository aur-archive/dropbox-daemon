# Maintainer: David J. Haines <djhaines@gmx.com>
# Contributor: Jason St. John <jstjohn@purdue.edu>
# Contributor: Tim Gerhard <tim-gerhard@schnellbach-beltheim.de>
# Contributor: TechliveZheng <techlivezheng@gmail.com>

pkgname=dropbox-daemon
pkgver=0.8
pkgrel=8
pkgdesc="Run Dropbox as a given user at boot."
arch=('any')
# Note: This URL is the home page from a previous maintainer, sylar_5.
url="http://dl.dropbox.com/u/8192972/arch_pacs/dropbox-daemon.html"
license=('MIT')
depends=('dropbox')
conflicts=('dropboxd-userspace')
replaces=('dropboxd-userspace')
backup=('etc/conf.d/dropboxd.conf')
install=dropbox-daemon.install
source=('dropboxd' 'dropboxd.conf')
md5sums=('d0a8cf67b543d4cbc42a7239e569c6df' '53480a6bcd6fb0bfcb5f30741177a595')

package() {
  cd "${srcdir}"
  mkdir -p "${pkgdir}/etc/conf.d/"
  mkdir -p "${pkgdir}/etc/rc.d/"
  install -m644 dropboxd.conf "${pkgdir}/etc/conf.d/"
  install -m755 dropboxd "${pkgdir}/etc/rc.d/"
}

# vim:set ts=2 sw=2 et:
