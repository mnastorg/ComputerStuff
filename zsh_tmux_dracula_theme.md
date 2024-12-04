# Enhance terminal with Zsh, Tmux and Dracula

## For Dracula theme
Dracula theme available in https://draculatheme.com/. In the terminal settings, create new profile for the dracula theme and set it as default. Then, in the Dracule site, find Gnome-terminal and follow the installation steps.

## For Zsh

Zsh, short for Z Shell, is a feature-rich Unix-like shell. It’s a great fit for users who need an interactive experience for task execution and scripting. It offers many improvements over traditional shells like sh and Bash. Install zsh if it is not already done by default. Follow the instruction in https://github.com/ohmyzsh/ohmyzsh/wiki/Installing-ZSH, and make sure zsh is the default shell.

Oh My Zsh is an open source, community-driven framework for managing your zsh configuration (Github: https://github.com/ohmyzsh/ohmyzsh). To install oh my zsh, run:
    
    sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"

Once oh my zsh is installed, add the autosuggestion and syntax highlighting plugins (Github: https://github.com/zsh-users/zsh-autosuggestions/tree/master and https://github.com/zsh-users/zsh-syntax-highlighting). To install auto-suggestions and syntax-highlighting, run:

    git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions

    git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting 

Add the plugins, by changin the plugin line in ~/.zshrc:

    vi ~/.zshrc 
    
Find the plugins line and replace with:
    
    plugins=(git zsh-autosuggestions zsh-syntax-highlighting)

Install powerlevel10k theme for oh my zsh. p10k emphasizes speed, flexibility and out-of-the-box experience (Github of powerlevel10k https://github.com/romkatv/powerlevel10k). First change the fonts by downloading the Meslo file in https://github.com/kgraefe/meslo-lgsn-patched. Once it is download, open it and install it. Then go in Terminal setting, change the font to Meslo. To install p10k, run:

    git clone --depth=1 https://github.com/romkatv/powerlevel10k.git ${ZSH_CUSTOM:-$HOME/.oh-my-zsh/custom}/themes/powerlevel10k

Then, in ~/.zshrc, set ZSH_THEME="powerlevel10k/powerlevel10k". Update by running

    source ~/.zshrc

or 

    exec zsh

To configure the theme, run the following command and follow the instructions:

    p10k configure
    
Additional note if using CONDA: in ~/.bashrc (original bash shell) copy the script part about conda and paste it in ~/.zshrc. In the Github of p10k, search for colors section if you want to change colors.

## For Tmux

Tmux est un multiplexeur de terminaux, outil permettant d'exploiter plusieurs terminaux au sein d'un seul et même affichage. Si il n'est pas installer par défaut, il faut installer le paquet tmux. See the doc for more info on how to use it : https://doc.ubuntu-fr.org/tmux
