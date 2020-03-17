# Maintainer: TBK <aur at jjtc dot eu>
# Contributor: TBK <aur at jjtc dot eu>

pkgname=redo-c
pkgver=0.9.0
pkgrel=1
pkgdesc='An implementation of the redo build system in portable C with zero dependencies'
url='https://github.com/leahneukirchen/redo-c'
arch=('x86_64')
license=('CC0-1.0')
conflicts=('redo-c-git' 'redo-jdebp' 'redo-python' 'redo-sh')
makedepends=('gcc')
source=("$pkgname-$pkgver.tar.gz::https://github.com/tbk/redo-c/archive/$pkgver.tar.gz") 
sha256sums=('b7b68a9768db6f09745a6055f13513e7b05494b0916d0c4e00d38872b5bbd2ef')
_builddir="$pkgname-$pkgver"

build() {
	cd "$_builddir"
	gcc -g -Os -Wall -Wextra -Wwrite-strings -o redo redo.c
}

package() {
	cd "$_builddir"
	DESTDIR="$pkgdir" ./redo install
}
