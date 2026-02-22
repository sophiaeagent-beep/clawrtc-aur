# Maintainer: Elyan Labs <scott@elyanlabs.ai>
pkgname=clawrtc
pkgver=1.6.0
pkgrel=1
pkgdesc="Mine RTC tokens with your AI agent - RustChain Proof of Antiquity consensus"
arch=('any')
url="https://bottube.ai"
license=('MIT')
depends=('python' 'python-requests')
makedepends=('python-build' 'python-installer' 'python-wheel' 'python-setuptools')
source=("https://files.pythonhosted.org/packages/source/c/clawrtc/clawrtc-${pkgver}.tar.gz")
sha256sums=('2c94df74f1647d5f3a245a288936687cba41e770da392808c2eff36e653d5d24')

build() {
    cd "$srcdir/clawrtc-$pkgver"
    python -m build --wheel --no-isolation
}

package() {
    cd "$srcdir/clawrtc-$pkgver"
    python -m installer --destdir="$pkgdir" dist/*.whl
    install -Dm644 LICENSE "$pkgdir/usr/share/licenses/$pkgname/LICENSE"
}
