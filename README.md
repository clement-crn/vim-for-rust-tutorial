# vim-for-rust-tutorial
![vim-rust2](https://user-images.githubusercontent.com/86530475/212573566-87a8b2de-a7f4-4550-97c5-0a54d6383b03.jpg)

ONLY FOR MAC OS

| Our recipe   | 
| ------------- | 
| vim-plug | 
| coc.nvim  | 
| rust-analyzer | 
| YouCompleteMe | 

**Install Vim-Plug**

Vim-Plug is necessary for coc.
```
curl -fLo ~/.vim/autoload/plug.vim --create-dirs \
    https://raw.githubusercontent.com/junegunn/vim-plug/master/plug.vim
```

**Install coc.nvim**

Install node
```
curl -sL install-node.vercel.app/lts | bash
```

Add these lines in your .vimrc file

Make the *autoload* folder in ~/.vim/ if you don't have one already


```vim
Plug 'neoclide/coc.nvim', {'branch': 'release'}
Plug 'neoclide/coc.nvim', {'branch': 'master', 'do': 'yarn install --frozen-lockfile'}

call plug#begin('======YOURPATHTOAUTOLOAD======') 
Plug 'neoclide/coc.nvim', {'branch': 'release'}

Plug 'neoclide/coc.nvim', {'branch': 'master', 'do': 'yarn install --frozen-lockfile'}
call plug#end()
```

☝🏻 **In the *.vimrc* file do not forget to specify the path to the autoload folder**

In my case, the line should be :

```
call plug#begin('~/.vim/autoload')
```


*Wait, how to access my vimrc file ?*

<details>
In your terminal

```
cd
vim ~/.vimrc 
```


</details>

Add everything from here in your *autoload* folder:

https://github.com/neoclide/coc.nvim/tree/master/autoload

*reminder : it should be in*
```
~/.vim/autoload
```

3-Restart vim and type:

```
:PlugInstall
```
**Install rust-analyzer**

```
:CocInstall coc-rust-analyzer
```

**Install YouCompleteMe**

```
$ brew install cmake python go nodejs
```

Go to

```
~/.vim/
```

Then

```
mkdir bundle
cd bundle
mkdir YouCompleteMe
```

Then we will download the *install.py* file from YouCompleteMe github page.
I chose to not upload here since he might be updated.

https://github.com/ycm-core/YouCompleteMe#installation

Now, we need to run the script this way :

```
cd ~/.vim/bundle/YouCompleteMe
python3 install.py --rust-completer
```

You can now impress everyone with your fancy vim, good job.

I will be glad to help you with your issues.


Links for more details:

https://github.com/junegunn/vim-plug

https://github.com/neoclide/coc.nvim

https://rust-analyzer.github.io

https://github.com/VundleVim/Vundle.vim#about

https://github.com/ycm-core/YouCompleteMe

https://cmake.org
