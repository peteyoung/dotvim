__NOTE:__ I've abandoned pathogen in favor of vundle. vundle plays nicer with initial setup of a box. I have one less repo to worry about (dotfiles only vs. dotfiles and dotvim).

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

Add a new plugin as git submodule in .vim/bundle
------------------------------------------------
```bash
cd ~/.vim
git submodule add https://github.com/<account>/<plugin-repo>.git bundle/<plugin-name>
git add .
git commit -m "Install <plugin-name> bundle as a submodule."
```

Update all plugins and pathogen
-------------------------------
```bash
cd ~/.vim
git submodule foreach git pull origin master
```

Update an individual plugin
---------------------------
```bash
cd ~/.vim/bundle/foo
git pull origin master
```

Add pathogen as git submodule in .vim/pathogen
----------------------------------------------
```bash
cd ~/.vim
git submodule add https://github.com/tpope/vim-pathogen.git pathogen
ln -s ~/.vim/pathogen/autoload/pathogen.vim ~/.vim/autoload/pathogen.vim
```


