# Maintainer: Krystian Soltysik <krystians@outlook.com>
pkgname=hunalign-1.1
pkgver=1.1
pkgrel=1
pkgdesc="hunalign – sentence aligner"
arch=(i686 x86_64)
license=('LGPL2.1')
makedepends=(gcc make)
depends=(gcc-libs-multilib python bash gawk)
source=("ftp://ftp.mokk.bme.hu/Hunglish/src/hunalign/latest/hunalign-1.1.tgz")
md5sums=('0e372362414b8acebca7898063d6a3a6')
url='"http://mokk.bme.hu/resources/hunalign/'      

build() {
  cd "${srcdir}/${pkgname}"/src/hunalign
  make 
  mkdir -p "${pkgdir}"/usr/bin
  mkdir -p "${pkgdir}"/opt
} 

 package() {
cd ${srcdir}/${pkgname}
for f in `find -type f`; do
  install -D "$f" "${pkgdir}/opt/hunalign/$f"
done
ln -sf "${pkgdir}/opt/hunalign/src/hunalign/hunalign" "${pkgdir}/usr/bin/hunalign"
}
