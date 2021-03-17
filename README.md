# vim-config
My VIM configuration 



### Vim folder permissions
In VIM main folder - In my case: /etc/vim - set full permissions to vimrc with command:
- chmod 777 vimrc


### Install Pluggin Manager

Using PLUG from web https://github.com/junegunn/vim-plug

curl -fLo ~/.vim/autoload/plug.vim --create-dirs https://raw.githubusercontent.com/junegunn/vim-plug/master/plug.vim
  


### On error: [coc.nvim] "node" is not executable, checkout https://nodejs.org/en/download/
Primero actualizamos nuestro entorno y luego instalamos nodejs
- sudo apt-get update
- sudo apt-get upgrade
- sudo apt-get install nodejs
- sudo apt-get install npm

### Instalamos paquetes de idiomas de coc mediante comando: CocInstall:
- CocInstall coc-json coc-tsserver coc-html coc-css coc-python
