# Contributor: Anonymous
# Generator  : CPANPLUS::Dist::Arch 1.29

pkgname='perl-poe-component-client-ping'
pkgver='1.174'
pkgrel='1'
pkgdesc="a non-blocking ICMP ping client"
arch=('any')
license=('PerlArtistic' 'GPL')
options=('!emptydirs')
depends=('perl-poe>=1.007')
makedepends=()
url='http://search.cpan.org/dist/POE-Component-Client-Ping'
source=('http://search.cpan.org/CPAN/authors/id/R/RC/RCAPUTO/POE-Component-Client-Ping-1.174.tar.gz')
md5sums=('93c50b99d5476b6596ff24800a7b0c8a')
sha512sums=('f12c5e32239935996aaf4597068b7807ab923858341e342a622fd66a3cb6d92503ae53f6606e92efb1dade56e153c0b7e816b844479d2b77bb0e7378c37ec315')
_distdir="POE-Component-Client-Ping-1.174"

build() {
  ( export PERL_MM_USE_DEFAULT=1 PERL5LIB=""                 \
      PERL_AUTOINSTALL=--skipdeps                            \
      PERL_MM_OPT="INSTALLDIRS=vendor DESTDIR='$pkgdir'"     \
      PERL_MB_OPT="--installdirs vendor --destdir '$pkgdir'" \
      MODULEBUILDRC=/dev/null

    cd "$srcdir/$_distdir"
    /usr/bin/perl Makefile.PL
    make
  )
}

check() {
  cd "$srcdir/$_distdir"
  ( export PERL_MM_USE_DEFAULT=1 PERL5LIB=""
    make test
  )
}

package() {
  cd "$srcdir/$_distdir"
  make install
  find "$pkgdir" -name .packlist -o -name perllocal.pod -delete
}

# Local Variables:
# mode: shell-script
# sh-basic-offset: 2
# End:
# vim:set ts=2 sw=2 et:
