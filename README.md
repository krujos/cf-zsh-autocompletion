cf-zsh-autocompletion
=======================

Oh My Zsh (or probably any zsh but YMMV) plugin for cf (Cloud Foundry) autocompletion. 

See the know issues below for what doesn't work.

#Installation 

Drop the ```cf``` directory into your ```$ZSH/custom/plugins/``` (usually ```~/.oh-my-zsh/custom/plugins```) directory. Then add cf to the plugins line of your ```.zshrc``` file. For example here's my ```.zshrc``` plugin lines

    # Which plugins would you like to load? (plugins can be found in ~/.oh-my-zsh/plugins/*)
    # Custom plugins may be added to ~/.oh-my-zsh/custom/plugins/
    # Example format: plugins=(rails git textmate ruby lighthouse)
    # Add wisely, as too many plugins slow down shell startup.
    plugins=(git docker jsontools tmux vagrant bosh cf)
  
#Runtime Options
Personally I think the short hand options to many CF commands clutter up the tab view, so I don't include them in the default output. If you want them included in the output ```export CF_ZSH_INCLUDE_SHORT=true```. The plugin will look for this variable every time so if you want to play with it you an set it on the command line. Otherwise, stick it in your ```.zshrc``` had have at it.
    

#Example

Type ```cf <tab>``` and watch the magic happen

    ➜  ~  cf <tab>                                                                      
    zsh: do you wish to see all 120 possibilities (60 lines)? y                                                
    api                                     passwd
    app                                     plugins
    apps                                    purge-service-offering
    auth                                    push
    bind-running-security-group             quota
    ... and on and on
    
    ➜  ~  cf create-<tab>                                                                                                  
    create-buildpack              create-security-group         create-space
    create-domain                 create-service                create-space-quota
    create-org                    create-service-auth-token     create-user
    create-quota                  create-service-broker         create-user-provided-service
    create-route                  create-shared-domain

	
#Known Issues
It doesn't provide extended help for commands, which would be nice. For instance when you type ```cf push <tab>``` you don't get the usage. 

It doesn't know about parameters yet, so it won't prompt you for everything you need in the create-user-provided-service command.  

#El Problemo? 
Open an issue or submit a PR please!


#Tracker
[Is avaliable here](https://www.pivotaltracker.com/n/projects/1239006)