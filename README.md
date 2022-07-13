### Extract your files⚠️

| Distro | Description |
| ------ | ------ |
| Debian / Ubuntu |  sudo apt update && sudo apt install unrar p7zip-full p7zip-rar unzip gzip |
| Fedora |  sudo dnf install p7zip p7zip-plugins unrar unzip gzip |	
| Arch |  yay -S 7-zip && sudo pacman -S unrar unzip gzip |

# Install

* Open The Terminal .
* Add this code in your bash / zsh profile 
	
nano .bashrc

nano .zshrc


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



### Visita el tutorial para mas detalles
[![Alt text](https://i.postimg.cc/pT6YVfxf/extract.png)](https://youtu.be/0v2T1pQnDAI)


### Issues will be fixed asap. Pull Request Welcomed
https://github.com/callmezatiel/extract/issues

### Buy me a coffee
<a href="https://www.paypal.me/zatiel"><img src="https://img.shields.io/badge/don-paypal-blue"></a> <a href="https://www.patreon.com/zatiel"><img src="https://img.shields.io/badge/don-patreon-ff69b4">
