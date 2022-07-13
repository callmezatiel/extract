### Extract your files⚠️

| Distro | Description |
| ------ | ------ |
| Debian / Ubuntu |  sudo apt update && sudo apt install unrar p7zip-full p7zip-rar unzip gzip |
| Fedora |  sudo dnf install p7zip p7zip-plugins unrar unzip gzip |	
| Arch |  yay -S 7-zip && sudo pacman -S unrar unzip gzip |

	
nano .bashrc


```
# add this to easily extract compressed files, use extract <filename> to extract 

extract () {
    if [ -f $1 ] ; then
            case $1 in
            *.tar.bz2)    tar xvjf $1    ;;
            *.tar.gz)    tar xvzf $1    ;;
            *.tar.xz)    tar xf $1      ;;
            *.bz2)        bunzip2 $1     ;;
            *.rar)        unrar x $1     ;;
            *.gz)        gunzip $1      ;;
            *.tar)        tar xvf $1     ;;
            *.tbz2)        tar xvjf $1    ;;
            *.tgz)        tar xvzf $1    ;;
            *.zip)        unzip $1       ;;
            *.Z)        uncompress $1  ;;
            *.7z)        7z x $1        ;;
            *)        echo "don't know how to extract '$1'..." ;;
            esac
    else
            echo "'$1' is not a valid file!"
    fi
 }
```

Try:
extract folders.tar.gz
