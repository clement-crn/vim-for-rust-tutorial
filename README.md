# vim-for-rust-tutorial
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

1-Install node
```
curl -sL install-node.vercel.app/lts | bash
```

2-Add these lines in your .vimrc file.

```
Plug 'neoclide/coc.nvim', {'branch': 'release'}
Plug 'neoclide/coc.nvim', {'branch': 'master', 'do': 'yarn install --frozen-lockfile'}
```
*Wait, how to access my vimrc file ?*

<details>
In your terminal

```
cd
```

```
vim ~/.vimrc 
```


</details>

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







