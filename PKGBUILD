# Maintainer: Tom Oliver <t.l.oliver@protonmail.com>

pkgname=towm
pkgver=0.2.2
pkgrel=1
pkgdesc="Tom Oliver's Window Manager."
url="https://github.com/tomoliverxyz/towm"
license=("MIT")
arch=("x86_64")
depends=('git' 'base-devel' 'xorg-server' 'xorg-xinit' 'libxft' 'libxinerama' 'noto-fonts' 'ttf-font-awesome' 'confuse' 'xterm' 'dmenu')
provides=('towm')
source=("towm-$pkgver.tar.gz::$url/releases/download/v$pkgver/$pkgname-$pkgver.tar.gz")
sha256sums=('3e7a2411b60d1454837233c8e32b06e1bd5b95ff2ac94c5bb796e8587f5d41dd')

package() {
	cd $pkgname-$pkgver
	# build towm
	sudo make
	# make sure source lives in /usr/local/share/towm
	sudo make setup
	# install binary of towm
	sudo make install
}
