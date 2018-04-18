## Intro

I'm currently a Ruby/Rails/iOS app developer and instructor, this is my personal Vim configurations and some plugins which I used in my daily job, and I removed and reorganized redundant settings and plugins from my another vim repository https://github.com/kaochenlong/eddie-vim

I put Vim related settings in `plugin/settings/settings.vim`, and isolated other plugins' settings in `plugin/settings` directory.

You might notice that there are several vimrc files:

1. `vimrc`, standard version vimrc.
2. `vimrc_easy`, same as vimrc, but add some easier key mapping for new Vimer.
3. `vimrc_pro`, same as vimrc, but remove the arrow keys mapping.
4. `vimrc_experimental`, same as pro-vimrc, but just for experimental purpose.

you can make a symbolic link of your `~/.vimrc` to any one of them as you wish :)

my Vim looks like:

![image](https://raw.githubusercontent.com/kaochenlong/eddie-vim2/master/screenshots/vim.png)

color theme: <a href="http://ethanschoonover.com/solarized" target="blank">solarized dark</a>

## Usage

### Installation and Requisites:

#### Automatic installer... (DO YOU TRUST ME?)

If you already install `git` in your machine, and you trust me and my automatic install shell script, you can install my vimrc via `curl` or `wget`, just copy one of the following line and paste in terminal:

1. via `curl`:

    `sh <(curl -L https://github.com/kaochenlong/eddie-vim2/raw/master/utils/install.sh)`

2. or via `wget`:

    `sh <(wget --no-check-certificate https://github.com/kaochenlong/eddie-vim2/raw/master/utils/install.sh -O -)`

#### Manual installation

1. BACKUP your `.vim` directory and `.vimrc` first.(IMPORTANT!)
2. `cd ~` to change directory to your home directory.
3. copy files to your home directory:

   `git clone git://github.com/kaochenlong/eddie-vim2.git .vim`

4. make a symbolic link to vimrc:

        ln -s .vim/vimrc .vimrc

5. if you're still not familiar with the movements in vim by HJKL or yanking and pasting text, I've made a easier version:

        ln -s .vim/vimrc_easy .vimrc

6. if you use GUI version VIM, such as MacVim or GVim, you can also link to `.gvimrc`:

        ln -s .vim/gvimrc .gvimrc

7. if you use Airline under Ubuntu or something which can not show the correct icons/fonts on the bottom, you can check [this link](https://github.com/Lokaltog/powerline-fonts), patch the font and it should look pretty nice.

8. you might need to install `ack` or `silver searcher` if you use `ack.vim`.

### Features and Key Mappings:

0. my `<leader>` key is `\`.

1. Toggle between working mode and presentation mode by `<leader>z`, but it only works in GUI version Vim. You can check [here](http://blog.eddie.com.tw/2012/03/14/switch-to-presentation-mode/) to see how it looks like.

2. some usually used key mappings in normal mode:

    * `<F2>` to toggle NERDTree on and off.
    * `<F4>` to toggle Taglist window.
    * `<F5>` is the script runner, according to it's filetype, it will run Ruby(\*.rb) ,Python(\*.py) or PHP(\*.php) file, even CoffeeScript(\*.coffee, but you may have to install CoffeeScript first). If the filetype is VimScript, `<F5>` will reloadrun `:source %` and reload the current file.
    * hit `<ctrl>p` will launch a quick window to match keywords from your current working directory, not only file name, but also path name.
    * hit `<leader>` twice to toggle comment on and off.
    * `<tab>` and `<shift><tab>` to increase and decrease the syntax identation.

3. Remove tailing whitespace automatically while saving.

## FAQ

if you can not found `ctags` command, just find your ctags path and replace my settings in `plugin/settings/ctags.vim` file:

    let Tlist_Ctags_Cmd = '/your/path/to/ctags'

and [Exuberant Ctags](http://ctags.sourceforge.net/) is recommended.

## Contact

Enjoy it, and if there's any question or comment, feel free to let me know, or just fire an issue here :)

Eddie Kao (eddie@digik.com.tw)

