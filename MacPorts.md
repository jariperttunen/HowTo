# Some useful commands with MacPorts
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
+ port variants \<port\> (ports may have diverse installation options)
+ sudo port selfupdate (every two weeks or so)
  + sudo port upgrade outdated

# Xcode related commands
+ xcodebuild -showsdks (show installed developer kits)
+ xcode-select --install (install command line tools)
+ ls -Flah /Applications/Xcode.app/Contents/Developer/Platforms/MacOSX.platform/Developer/SDKs (sdk location)

# Some installations with MacPorts 
## Installation on macOS Big Sur, Intel processor. 
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
+ sudo port install cgal4 (old version, conflicts cgal5)
+ sudo port install cgal5 (new version, conflicts cgal4)
+ sudo port install doxygen
  + sudo port install graphviz
+ sudo port install texlive +full (LaTeX, full variant, i.e. full installation, may take awhile)
+ sudo port install TeXShop4 (LaTeX gui and editor)
+ sudo port install LyX (LateX WYSIWYM editor, "what you see is what you mean")
+ sudo port install ImageMagick 
+ sudo port install cvs
+ sudo port install enscript

#### Broken ports 
The following ports, at least, seem to be currently broken (macOS Big Sur)
+ paraview (download from https://paraview.org)

## X11 Window system
MacPorts has older version of XQuartz in **xorg** port. It has problems at least with OpenGL. 
Download from https://www.xquartz.org instead.

## Apple M1 processor
MacPorts ports for the new M1 processor seem to be under construction. You may try Rosetta 2.
The workaround is to first [create a Rosetta Terminal](https://dev.to/courier/tips-and-tricks-to-setup-your-apple-m1-for-development-547g) and then install Macports. Macports should install Intel versions of ports that are run through Rosetta 2.

# MacPorts behind firewall (proxies)
The easy way is to do MacPorts installations outside firewall. Otherwise one can set 
the three required environmental variables (in Terminal)

+ export RSYNC_PROXY=\<proxy_server\>:\<port\>
+ export HTTPS_PROXY=https://\<proxy_server\>:\<port\>
+ export HTTP_PROXY=http://\<proxy_server\>:\<port\>
+ sudo -E port \<command\>:
  + sudo -E port selfupdate
  + sudo -E port upgrade outdated

The `-E` option for `sudo` passes the three environmental variables to port command. 
If feasible the three export commands can be in the `.profile` or `.zprofile` files (bash/zsh shell respectively). 
A more advanced way to bypass firewall can be done with [Git](https://trac.macports.org/wiki/howto/SyncingWithGit).
