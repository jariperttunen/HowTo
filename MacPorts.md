## Some useful commands with MacPorts
+ port search \<keyword\>
+ port list installed
  + port installed inactive  
+ port info \<package\>
+ port variants \<package\>
+ sudo port install \<package\>
+ sudo port clean \<package\> (remove compilation files)
+ sudo port uninstall \<package\>
  + sudo port uninstall inactive (reclaim space by removing inactive ports) 
+ sudo port selfupdate (every two weeks or so)
+ sudo port upgrade outdated
+ port info --maintainers <package> (bug report: add maintainers if any)

## Xcode related commands
+ xcodebuild -showsdks (show installed developer kits)
+ xcode-select --install (install command line tools)
+ ls -Flah /Applications/Xcode.app/Contents/Developer/Platforms/MacOSX.platform/Developer/SDKs (sdk location)

## Some installations with macports 
I have managed to install these ports below including their dependencies. 
Major macOS updates may break ports (e.g. qt4).

+ sudo port install emacs-mac-app
+ sudo port install cvs

+ sudo port install cgal4 (old version)
+ sudo port install cgal5 (new version)

+ sudo port install python\<version\> (e.g. python39)
+ sudo port install R-app

+ sudo port install gcc\<version\> (e.g. gcc9)
  + sudo port select --set gcc mp-gcc\<version\> (e.g. mp-gcc9, gfortran ready to use)

+ sudo port install qt4-creator-mac (qt4 developer)

+ sudo port install doxygen
+ sudo port install graphviz

+ sudo port install texlive +full (LaTeX, full variant, i.e. full installation, may take awhile)

+ sudo port install ImageMagick 

I found the following ports are currently broken (macOS Big Sur)

+ paraview


