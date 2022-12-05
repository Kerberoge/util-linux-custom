pkgname=util-linux-custom
pkgver=2.38.1
pkgrel=1
pkgdesc="Custom util-linux package"
arch=('x86_64')
url="https://github.com/Kerberoge/util-linux-custom"
license=('GPL2')
provides=('rfkill' 'hardlink' 'util-linux')
conflicts=('rfkill' 'hardlink' 'util-linux')
replaces=('rfkill' 'hardlink' 'util-linux')
source=("https://archive.archlinux.org/packages/u/util-linux/util-linux-$pkgver-$pkgrel-$arch.pkg.tar.zst")
sha256sums=('a76f268571ea295f9e5e07be7ae24691f807fef57d5bb2e9fb59fc2cbcd9a5c3')

package() {
	rm $srcdir/usr/bin/more \
	$srcdir/usr/share/man/man1/more.1.gz \
	$srcdir/usr/share/bash-completion/completions/more

	rm $srcdir/usr/bin/su \
	$srcdir/usr/share/man/man1/su.1.gz \
	$srcdir/usr/share/bash-completion/completions/su \
	$srcdir/etc/pam.d/su \
	$srcdir/etc/pam.d/su-l

	cp -r $srcdir/usr $pkgdir
	cp -r $srcdir/etc $pkgdir
}
