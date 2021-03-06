# vim-config
My VIM configuration 



### Vim folder permissions
In VIM main folder - In my case: /etc/vim - set full permissions to vimrc with command:
- chmod 777 vimrc


### Install Pluggin Manager

Using PLUG from web https://github.com/junegunn/vim-plug
```
curl -fLo ~/.vim/autoload/plug.vim --create-dirs https://raw.githubusercontent.com/junegunn/vim-plug/master/plug.vim
 ```
Run Install
```
:PlugInstall
```


### On error: [coc.nvim] "node" is not executable, checkout https://nodejs.org/en/download/
Primero actualizamos nuestro entorno y luego instalamos nodejs
```
sudo apt-get update
sudo apt-get upgrade
sudo apt-get install nodejs
sudo apt-get install npm
 ```

### Install coc packages with CocInstall
- CocInstall coc-json coc-tsserver coc-html coc-css coc-python coc-pyright
- CocInstall coc-pairs
- CocConfig setup: 
```
{
	"pairs.enableCharacters": [
		"(",
		"[",
		"{",
		"'",
		"\"",
		"`"
	],
	"suggest.noselect": false,
	"coc.preferences.formatOnSaveFiletypes": [
		"javascript",
		"typescript",
		"typescriptreact",
		"json",
		"javascriptreact",
		"typescript.tsx",
		"graphql",
		"python"
	],
	"python.jediEnabled": false
}
```
- *"python.jediEnabled":false* is in test

### Install Kite
- If using Linux o WSL use the command: bash -c "$(wget -q -O - https://linux.kite.com/dls/linux/current)"
- If using Windows or OS download from kite's web page
- Follow https://github.com/kiteco/vim-plugin/blob/master/DEVELOPMENT.md to configure kite once installed

### WSL yank support
Install gvim: 
```
sudo apt-get install vim-gtk
```

### NeoVim config
```
sudo apt-get install neovim

```
If ~/.config/nvim/init.vim we have to create it:
```
mkdir ~/.config/nvim
touch ~/.config/nvim/init.vim
```
Edit init.vim with:
```
set runtimepath^=~/.vim runtimepath+=~/.vim/after
let &packpath=&runtimepath
source /etc/vim/vimrc
```
