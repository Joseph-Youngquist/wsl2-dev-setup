# Starting up a new WSL2 linux instance for development

## download Ubuntu
For this I've opted to use Ubuntu 18.04 due to broader support on the tech stack I'm wanting to use (couchbase).

Once download is complete opt to run it so you can make your first user account and password.


## apt update && apt upgrade
`sudo apt update && sudo apt upgrade`

## Development tools
### This blog post has lots of ideas that I lifted
#### (Windows Terminal - ya, you gotta have that! git, oh my zsh, etc.,)

[WSL2: Making Windows 10 the perfect dev machine!](https://partlycloudy.blog/2020/06/05/wsl2-making-windows-10-the-perfect-dev-machine/)

#### for Oh My zsh
I like to update my `~/.zshrc` file with the following updates
`export PATH=$HOME/bin:/usr/local/bin:$HOME/.local/bin:$PATH`
`ZSH_THEME="muse"`
`plugins=(git django docker python)`

### Docker in WSL2
[Using Docker in WSL 2](https://code.visualstudio.com/blogs/2020/03/02/docker-in-wsl2)

### VS Code
If you have Code installed on your windows side then I believe all you need to do inside your WSL instance is `code .`
and things magically happen, like:
```
Installing VS Code Server for x64 (e790b931385d72cf5669fcefc51cdf65990efa5d)
Downloading: 100%
Unpacking: 100%
Unpacked 2341 files and folders to /home/joe/.vscode-server/bin/e790b931385d72cf5669fcefc51cdf65990efa5d.
```
(I did say magic!)

### NVM (Node Version Manager)
`curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.35.3/install.sh | zsh` (or replace `zsh` for `bash` if you're not using zsh)
 Then install the node of your choice. I installed `v10.22.1` since that's what is currently (09/2020) running on Google Cloud Functions.

### Python and pipenv setup

On my system after the `upgrade` I had `python3 --version` of `3.6.9`

For a guide on all of this check out: [The Hitchhiker’s Guide to Python!](https://docs.python-guide.org/starting/install3/linux/#install3-linux)
I ran `sudo apt install python3.8`

#### pipenv
Following: 
[Pipenv & Virtual Environments](https://pipenv.pypa.io/en/latest/install/#installing-pipenv)

I like pipenv vs 

I had to install `pip` manually.
[]()
`curl https://bootstrap.pypa.io/get-pip.py -o get-pip.py`
then
`python3 get-pip.py`

`pip install --user pipx`

`sudo apt install python3-venv`

then finally:
`pipx install pipenv`
