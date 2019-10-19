# CommandlineSpecifcLinuxDesktopConfigurations

## Installation
```
pacman -S zsh zsh-theme-powerlevel9k i3-wm i3status demu zsh-completions powerline powerline-fonts terminator tmux && \
wget https://raw.githubusercontent.com/zsh-users/zsh/master/Completion/Unix/Command/_tmux -P /usr/share/zsh/site-functions/
```

### Terminator Terminal
~/.config/terminator/config                                                                                                                                                                      
```
[profiles]                                                                                                                                                                                                       
   [[default]]                                                                                                                                                                                                  
   foreground_color = "#000000"                                                                                                                                                                                 
   background_color = "#FFFFFF"                                                                                                                                                                                 
   show_titlebar = false       
```
### zsh
~/.zshrc                                                                                                                                                                                         
```
export LANG="en_US.UTF-8"                                                                                                                                                                                       
source /usr/share/zsh-theme-powerlevel9k/powerlevel9k.zsh-theme                                                                                                                                                 
                                                                                                                                                                                                                
autoload -Uz compinit promptinit                                                                                                                                                                                
compinit                                                                                                                                                                                                        
promptinit                                                                                                                                                                                                     
                                                                                                                                                                                                               
export http_proxy=http://127.0.0.1:3128                                                                                                                                                                        
export https_proxy=http://127.0.0.1:3128                                                                                                                                                                       
export ftp_proxy=http://127.0.0.1:3128                                                                                                                                                                           
                                                                                                                                                                                                                 
export HTTP_PROXY=http://127.0.0.1:3128                                                                                                                                                                         
export HTTPS_PROXY=http://127.0.0.1:3128                                                                                                                                                                         
export FTP_PROXY=http://127.0.0.1:3128       
```
### oh-my-zsh
```
plugins=(git history ssh-agent tmux pipenv ansible)
```

### tmux

~/.tmux.cfg
```
# Kommandoeingabe mit Strg+a                                                                                                                       
set -g prefix C-a                                                                                                                                                                                              
# Beginne Fensterzaehlweise mit 1                                                                         
set -g base-index 1                                                                                      
# Anzahl  der Historyeintraege                                                                                                                                                                                 
set -g history-limit 10000                                                                               
# Beginne Pane Zaehlweise mit 1                                                                                                                                                   
set -g  pane-base-index 1                                                                                                                                                                                       
# Verwende die vi Tasten                                                                                  
set -g  mode-keys vi                                                                                                                                                                                     
#set -g  automatic-rename                                                                                                                                                                                       
# Lese die Konfiguration mit Strg+a R                                                                   
bind-key R source-file ~/.tmux.conf \; display "Reloaded tmux.conf"                                                                                                                                                
# Verwende das x um ein Pane zu schliessen                                                              
unbind x                                                                                                 
bind-key x kill-pane                                                                                                                                                                                           
# Verwende X um eine Session zu schliessen                                                              
bind-key X kill-session                                                                                             
# Strg+a | Fester vertikal                                                                                                                                                                     
bind-key | split-window -h                                                                                
# Strg+a - Fester vertikal                                                                                                                                 
bind-key - split-window -v                                                                                                                                                       
                                                                                    
# Verwende zsh als default Shell                                                                                                   
set-option -g default-shell /usr/bin/zsh                                                                                                                                       
                                         
######################                                                                                   
### DESIGN CHANGES ###                                                                                                                                                                                    
######################                                                                           
                                                                                                                                                           
set -g default-terminal "screen-256color"                                                                                                                                                   
                                                                                                
# loud or quiet?                                                                               
set-option -g visual-activity off                                                             
set-option -g visual-bell off                                                                
set-option -g visual-silence off                                                            
set-window-option -g monitor-activity off                                                  
set-option -g bell-action none                                                            
                                                                                         
# statusbar                                                                             
set -g status on                                                                       
set -g status-position top                                                            
set -g status-bg blue                                                                
set -g status-fg white                 
```
