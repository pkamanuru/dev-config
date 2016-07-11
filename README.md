## zsh
## spacemacs
## YCMD Setup Spacemacs
* Download YCMD engine and compile <br>
* Omnisharp build would probably fail , It can be avoided if you don't want CSHARP support <br>
* This will be our ycmd server and we should find a way to make emacs interact with this using a ycmd client ( emacs-ycmd ) which will interact with the emacs text completion framework company.
* There is one more plugin company-ycmd which provides advanced semantic completion unlike company.
* You need not go through the pain to setup all that if you have spacemacs, all you need to do is enable a few layers and point to a ycm configuration file and the ycm server location at which you compiled it.
* Enable ycmd, auto-completion and syntax checking layer in spacemacs <br>
* Setup ycmd-server-command. Given below is an example and you should point to your compiled directory <br>
```lisp
  (set-variable 'ycmd-server-command '("python" "~/Downloads/Tools/ycmd/ycmd/"))
```
* I set this variable in ycmd-init function of the ycmd layer - packages.el file. This can be done in user-config as well.
* Use a standard ycmd configuration, start with ycmd project's ycm configuration itself or the default config that comes with spacemacs <br>
* The default ycmd config exists here which is also the ycmd layer configuration folder for spacemacs
```bash
~/.emacs.d/layers/+tools/ycmd
```
* ycmd project's ycm configuration supports having a compile_commands.json file and works out of the box for all projects with a compilation database. You can search for the configuration file in ycmd's github repository with the same name ( global_conf.py ).
