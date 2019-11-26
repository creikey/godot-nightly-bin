# Maintainer: Cameron Reikes <cameronreikes@gmail.com>
pkgname=godot-nightly-bin
pkgver=3.2.beta
pkgrel=1
pkgdesc="Godot is an advanced, feature packed, multi-platform 2D and 3D game engine"
arch=("x86_64")
url="http://www.godotengine.org"
license=("MIT")
provides=("godot-nightly-bin")
depends=("fuse2")
source=("godot-nightly.desktop" "icons.tar.gz" "https://archive.hugo.pro/builds/godot/master/editor/godot-linux-nightly-x86_64.AppImage")
noextract=("godot-linux-nightly-x86_64.AppImage")
md5sums=("SKIP" "863b88ca5652e14fa68f0523e8dda65a" "SKIP")


package() {
  mkdir -p "$pkgdir/opt/$pkgname"
  mkdir -p "$pkgdir/usr/bin"
  mkdir -p "$pkgdir/usr/share/icons/hicolor"
  mkdir -p "$pkgdir/usr/share/applications"

  cp -L "$srcdir/godot-linux-nightly-x86_64.AppImage" "$pkgdir/opt/$pkgname/godot-nightly"

  cp -L "$srcdir/godot-nightly.desktop" "$pkgdir/usr/share/applications/godot-nightly.desktop"
  cp -L -a "$srcdir/icons/." "$pkgdir/usr/share/icons/hicolor"
  cp -L -a "$srcdir/icons/." "$pkgdir/usr/share/icons/gnome"

  chmod +x "$pkgdir/opt/$pkgname/godot-nightly"

  ln -s "/opt/$pkgname/godot-nightly" "$pkgdir/usr/bin/godot-nightly"
}
