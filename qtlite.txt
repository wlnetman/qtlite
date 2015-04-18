0. install msvc2013+update4 python2.7.8 activeperl5.20
refer qtcreator

1. open vc2013+update4 native-x86 cmd
git clone https://github.com/sunwangme/qtlite.git

2. cd qt5
git checkout 5.5
git submodule update --init --recursive

3. cd qt5
configure -prefix "c:\qtlite\qt5.5-vs12" -confirm-license -opensource -debug-and-release -shared -nomake tests -nomake examples -no-compile-examples -c++11 -ltcg -qt-sql-sqlite -plugin-sql-sqlite -no-freetype -no-opengl -no-qml-debug -no-icu -no-angle -qt-zlib -qt-libpng -qt-libjpeg -no-rtti -no-openssl -no-dbus -no-audio-backend -no-wmf-backend -no-style-windows -no-style-windowsxp -no-style-fusion -mp -platform win32-msvc2013
//-no-style-windowsvista 

4.cd qt5
nmake
nmake install

5.cd qt5
nmake docs
nmake install_docs
