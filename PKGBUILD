# Contributor: Michal Bozon <michal.bozon__at__gmail.com>

pkgname=python3-yaml
pkgver=3.09
pkgrel=1
pkgdesc="Python bindings for YAML, using fast libYAML library"
arch=('i686' 'x86_64')
url="http://pyyaml.org"
license=('MIT')
depends=('python3' 'libyaml')
provides=('python3-yaml')
conflicts=('python3-yaml-py' 'python3-yaml-libyaml')
install='python-yaml.install'
source=(http://pyyaml.org/download/pyyaml/PyYAML-$pkgver.tar.gz)
md5sums=('f219af2361e87fdc5e85e95b84c11d87')

build() {
  cd $srcdir/PyYAML-$pkgver
  python3 setup.py install \
    --prefix=/usr \
    --root=$pkgdir \
    || return 1
  install -m644 -D LICENSE $pkgdir/usr/share/licenses/$pkgname/LICENSE
}

