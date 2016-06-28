#Install undistract-me

https://github.com/jml/undistract-me


#Ubuntu 14.04 required the following added to .bashrc to get this working in bash terminal

```
. /usr/share/undistract-me/long-running.bash notify_when_long_running_commands_finish_install

if ! [ -z "$BASH_VERSION" -o -z "$PS1" -o -n "$last_command_started_cache" ]; then
  . /usr/share/undistract-me/long-running.bash
  notify_when_long_running_commands_finish_install
fi
```

#Getting the undistract-me to work in Zsh

Copy the notifyosd.zsh file to ~/.oh-my-zsh/custom/

and add this entry to .zshrc

```
source /usr/share/undistract-me/long-running.bash notify_when_long_running_commands_finish_install

[ -e $HOME/.oh-my-zsh/custom/notifyosd.zsh ] && . $HOME/.oh-my-zsh/custom/notifyosd.zsh
```


#Install sox for playing the audio files for notifications
sudo apt-get install sox libsox-fmt-all