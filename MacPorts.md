## Some useful commands with MacPorts
+ port help \[\<command\>\]
+ port search \<keyword\>
  + port search --exact \<keyword\>
+ sudo port install \<port\>
+ port list installed
  + port installed inactive 
+ sudo port clean \<port\> (remove compilation work)
+ sudo port uninstall \[--follow-dependencies\] \<port\>
  + sudo port uninstall inactive (reclaim space by removing inactive ports) 
  + sudo port uninstall installed
+ port info \<port\>
  + port info --maintainers (for bug report: add maintainers if any)    
+ port variants \<port\> (ports may have different installation options)
+ sudo port selfupdate (every two weeks or so)
  + sudo port upgrade outdated

## Xcode related commands
+ xcodebuild -showsdks (show installed developer kits)
+ xcode-select --install (install command line tools)
+ ls -Flah /Applications/Xcode.app/Contents/Developer/Platforms/MacOSX.platform/Developer/SDKs (sdk location)

## Some installations with MacPorts 
### Installation on macOS Big Sur, Intel. 

Major macOS updates may break ports (e.g. qt4 seems to be sensitive).

+ sudo port install emacs-mac-app
  + sudo port install ess (Emacs mode for statistical programming, R-mode, remote server use)   
+ sudo port install python\<version\> (e.g. python39)
  + sudo port select --set python\<version\> (active version)    
  + install python packages with pip 
+ sudo port install R-app
+ sudo port install gcc\<version\> (e.g. gcc9)
  + sudo port select --set gcc mp-gcc\<version\> (e.g. mp-gcc9, active version, gfortran ready to use)
+ sudo port install qt4-creator-mac (qt4 developer)
+ sudo port install cgal4 (old version)
+ sudo port install cgal5 (new version)
+ sudo port install doxygen
  + sudo port install graphviz
+ sudo port install texlive +full (LaTeX, full variant, i.e. full installation, may take awhile)
+ sudo port install TeXShop4 (LaTeX gui and editor)
+ sudo port install LyX (LateX WYSIWYM editor, "what you see is what you mean")
+ sudo port install ImageMagick 
+ sudo port install cvs
+ sudo port install enscript

The following ports, at least, seem to be currently broken (macOS Big Sur)
+ paraview (download from https://paraview.org)

MacPorts ports for M1 processor seem to be under construction.


