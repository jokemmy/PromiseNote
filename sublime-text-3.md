# Sublime Text 3

1. Download [Sublime Text 3](https://www.sublimetext.com/3) and setup
2. Install package control
  
  two ways
  
  * If you have not installed package control, choose `Tools -> Install package control`, and it will install automatically.
  * open console (``Ctrl+` ``), paste the code and run  
    
    ```bash
    import urllib.request,os; pf = 'Package Control.sublime-package'; ipp = sublime.installed_packages_path(); urllib.request.install_opener( urllib.request.build_opener( urllib.request.ProxyHandler()) ); open(os.path.join(ipp, pf), 'wb').write(urllib.request.urlopen( 'http://sublime.wbond.net/' + pf.replace(' ','%20')).read())
    ```
3. Install packages
  * open package controller (`ctrl+shift+p` or `Preferences -> Package Control`)
  * choose `Package Controll: Install package` and search plugins you want.

## plugins

`Alignment` `babel` `Emmet` `HTML5` `less` `sass` `DocBlockr` `BracketHighlighter`
`TrailingSpaces` `SublimeLinter` `SublimeLinter-contrib-eslint`
