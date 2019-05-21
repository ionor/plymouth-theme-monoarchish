pkgname=plymouth-theme-monoarchish
pkgver=0.1
pkgrel=1
pkgdesc='Modified monochrome Arch Linux theme for Plymouth'
arch=('any')
url='https://farsil.github.io/monoarch/'
license=('MIT')
depends=('plymouth')
install=$pkgname.install
source=("https://github.com/farsil/monoarch/archive/$pkgver.tar.gz"
        "$pkgname.install"
	'bullet.png'
	'lock.png'
	'box.png'
	'entry.png'
	'monoarchish.plymouth')
sha256sums=('e26fe7100dbe612b517037a55488f5ae25976b55e60a542c53623073e52a5ca1'
            'efc4134ab3a534dbd0b92ec1abc55f17cda2968c0d5c6a855fe0cb760b4b291a')

package() {

    # PATCH 
    mv -f *.png "$srcdir/monoarch-$pkgver/images/"
    mv -f monoarchish.plymouth "$srcdir/monoarch-$pkgver/"
    rm -f "$srcdir/monoarch-$pkgver/monoarch.plymouth"

    cd "$srcdir/monoarch-$pkgver"
                    
    install -d "$pkgdir/usr/share/plymouth/themes/monoarchish/images/" 
    install -Dm644 monoarchish.* "$pkgdir/usr/share/plymouth/themes/monoarchish/"
    install -Dm644 monoarch.* "$pkgdir/usr/share/plymouth/themes/monoarchish/"
    install -Dm644 images/* "$pkgdir/usr/share/plymouth/themes/monoarchish/images/"
    install -Dm644 LICENSE "$pkgdir/usr/share/licenses/$pkgname/LICENSE"
}
sha256sums=('e26fe7100dbe612b517037a55488f5ae25976b55e60a542c53623073e52a5ca1'
            'efc4134ab3a534dbd0b92ec1abc55f17cda2968c0d5c6a855fe0cb760b4b291a'
            '3cc843b334076922b3aaa562400a660c8ece3517a0f9091aeb41da3fcdf8abec'
            '232c23526722389afd42c278c6a31d2bdd3ca0e6207d54287c603938bbcd9e57'
            'c4d8517ed9f58273607d753284c660bd6e7cfc8caa3baa25dc419a8c1388aac2'
            '52f15ce4d1e7d7906e0909d033c69b8c102bc1feecde725721bf48e29e19ec6f')
sha256sums=('e26fe7100dbe612b517037a55488f5ae25976b55e60a542c53623073e52a5ca1'
            'efc4134ab3a534dbd0b92ec1abc55f17cda2968c0d5c6a855fe0cb760b4b291a'
            '3cc843b334076922b3aaa562400a660c8ece3517a0f9091aeb41da3fcdf8abec'
            '232c23526722389afd42c278c6a31d2bdd3ca0e6207d54287c603938bbcd9e57'
            'c4d8517ed9f58273607d753284c660bd6e7cfc8caa3baa25dc419a8c1388aac2'
            '52f15ce4d1e7d7906e0909d033c69b8c102bc1feecde725721bf48e29e19ec6f'
            '4dccb46745252aa0c505a7d1fa1dd6a5ae3a0e82e4d628c165121da2ecb7d580')
