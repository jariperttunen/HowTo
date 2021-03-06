## Some useful commands with MacPorts

+ port search \<keyword\>
+ port list installed
+ port info \<package\>
+ port variants \<package\>
+ sudo port install \<package\>
+ sudo port clean \<package\> (remove compilation files)
+ sudo port uninstall \<package\>

+ sudo port selfupdate (every two weeks or so)
+ sudo port upgrade outdated

## Some installations with macports 
I have manage to install these ports below including their dependencies. 
Major macOS updates may break ports (e.g. qt4).

+ sudo port install emacs-mac-app
+ sudo port install cvs

+ sudo port install cgal4 (old version)
+ sudo port install cgal5 (new version)

+ sudo port install python\<version\> (e.g. python39)
+ sudo port install R-app

+ sudo port install gcc\<version\> (e.g. gcc9)
  + sudo port select --set gcc mp-gcc\<version\> (e.g. mp-gcc9, gfortran)

+ sudo port install qt4-creator-mac (qt4 developer)

+ sudo port install doxygen
+ sudo port install graphviz

+ sudo port install texlive +full (LaTeX, full variant, i.e. full installation, may take awhile)

+ sudo port install ImageMagick 

I found the following ports are currently broken (macOS Big Sur)

+ paraview


