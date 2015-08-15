# Mantainer: danyf90 <daniele.formichelli@gmail.com>

pkgname=firefox-holly
pkgver=31.0a1
pkgrel=1
pkgdesc='Standalone web browser from mozilla.org, nightly build'
url='http://www.mozilla.org/projects/firefox'
arch=('i686' 'x86_64')
license=('MPL' 'GPL' 'LGPL')
depends=('alsa-lib' 'libxt' 'libnotify' 'mime-types' 'nss' 'gtk2' 'sqlite3' 'dbus-glib')
provides=("firefox=$pkgver")
conflicts=('firefox')
source=("http://ftp.mozilla.org/pub/firefox/nightly/latest-holly/firefox-$pkgver.en-US.linux-$CARCH.tar.bz2"
        "$pkgname.desktop"
        "$pkgname-safe.desktop")
sha512sums=('SKIP'
            'a3dd5c95ce887245adc975661d033b257f7751d04eaedad661ccd4355376e17042916074a07d22d4a9a44859a47b51ec296d78e1eef067b6148c47f9ff182b7a'
            'abb7c106524f669a0bf17507b45c3e5a35bbb45555c0d42664769862ed2e1cb1bd8ea8c7ba280bf726e381185dc471692e8a82c965c201fd0295f7693db6019c')

package() {
  install -d $pkgdir/{opt,usr/{bin,share/applications}}

  cp -r firefox $pkgdir/opt/firefox-holly

  ln -s /opt/firefox-holly/firefox $pkgdir/usr/bin/firefox-holly

  install -Dm644 $srcdir/{$pkgname.desktop,$pkgname-safe.desktop} $pkgdir/usr/share/applications/

  install -Dm644 $srcdir/firefox/browser/icons/mozicon128.png $pkgdir/usr/share/pixmaps/$pkgname-icon.png
}
