# Tmux config
My tmux configuration

### Installation

Start by cloning this repo to your linux machine and installing tmux

```bash
git clone --recurse-submodule https://github.com/btrvarun/tmux_config.git ~/.tmux/
ln -s ~/.tmux/.tmux.conf ~/.tmux.conf

# debian:
sudo apt install tmux

#arch-linux:
sudo pacman -S tmux
```

### Configuration


now add the following lines into your ~/.bashrc file
```
# TMUX scripting
if command -v tmux &> /dev/null && [ -n "$PS1" ] && [[ ! "$TERM" =~ screen ]] && [[ ! "$TERM" =~ tmux ]] && [ -z "$TMUX" ]; then
  exec tmux
fi

# To activate virtual environment if present
if [[ -d "venv" ]]; then
	source venv/bin/activate
fi
```

now activate the default bashrc script
```
exec bash
```

Tmux is open, Install the plugins by pressing: 

Ctrl+a I (capital i)

Your tmux is ready to go! Now follow my vim configuration instructions!
