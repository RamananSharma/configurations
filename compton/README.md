#installation of compton

$ sudo apt-add-repository ppa:richardgv/compton
$ sudo apt-get update
$ sudo apt-get install compton

#Add config file to ~/.config/compton.conf
config file samples are in repo

#Added the following to Session & Startup section
compton -b

-b flag demonizes the compton process and fork to background after initialization


#Find the name of the window to exclude from shadow
Type this command on terminal 

$ xwininfo -stats -wm


#Running compton without the config file,

Launch compton at startup with this command

compton --backend glx --paint-on-overlay --vsync opengl-swc -b
