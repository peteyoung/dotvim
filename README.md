Vim configuration and plugins
=============================

This is my vim setup using pathogen. All plugins are submodules existing under bundle/. Pathogen itself lives under pathogen and is symlinked to autoload/.

Installation
------------
```bash
cd ~
git clone http://github.com/peteyoung/dotvim.git ~/.vim
ln -s ~/.vim/vimrc ~/.vimrc
ln -s ~/.vim/gvimrc ~/.gvimrc
cd ~/.vim
git submodule init
git submodule update
```

Update all submodules
---------------------
```bash
cd ~/.vim
git submodule foreach git pull origin master
```

Update an individual module
---------------------------
```bash
cd ~/.vim/bundle/foo
git pull origin master
```

Add pathogen as git submodule in .vim
-------------------------------------
```bash
cd ~/.vim
git submodule add https://github.com/tpope/vim-pathogen.git pathogen
ln -s ~/.vim/pathogen/autoload/pathogen.vim ~/.vim/autoload/pathogen.vim
```


