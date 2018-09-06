# Installieren der Software
 - [Skim](https://sourceforge.net/projects/skim-app/):
     Siehe Webseite.
 - [MacVim](http://macvim-dev.github.io/macvim/):
     Mit [brew](https://brew.sh):
     ```
     $ brew install macvim
     ```

## Installieren von Skripten
 1. Füge das ReloadSkim Script in ein Verzeichnis der *$PATH* variable ein.
 1. Füge die Zeile
    ```vimscript 
    map <F11> :w<CR>:!make debug<CR>
    ```
    in *~/.vim/ftplugin/tex.vim* an.
 1. Setze Einstellung in: " *Skim -> Preferences... -> Sync -> PDF-Tex-Support -> 
    Preset* " zu MacVim

# Benutzen des Workflows
## Ordnerstruktur
 - Die *.tex* das  *make_open* Skript und das *makefile* müssen an derselben
Stelle gespeichert werden. 
 - Passe das makefile an, sodass der richtige Name der *.tex* ohne Endung in 
   der Variablen **S** steht.

## Benutzen des Workflows
Doppelklick auf *make_open* oder start im Terminal:
```
$ ./make_open
```
Um den Editor + PDF-Viewer(wenn schon eine PDF vorhanden ist) zu starten.
## Interagieren der Programme
 - Vim: Schnell kompilieren und Skim neu laden: **F11**
 - Vim: Final kompilieren **:!make**
 - Skim: **CMD+LShift+LMouse** um an die Stelle in Vim zu springen (bei Problemen
   mit Synctex einfach mal neu kompilieren).

# Empfohlene Plugins (für Vim)
 - [Syntastic](https://github.com/vim-syntastic/syntastic)
 - [vim-tex-syntax](https://github.com/gi1242/vim-tex-syntax)
