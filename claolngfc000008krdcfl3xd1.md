# Como colocar a branch atual no terminal do Linux

Para aparecer a branch atual do seu repositório GIT.

Primeiro abra o .bashrc:


```
nano ~/.bashrc
``` 

Depois insira o trecho: 


```
parse_git_branch() {
     git branch 2> /dev/null | sed -e '/^[^*]/d' -e 's/* \(.*\)/ (\1)/'
}
export PS1="\u@\h \[\033[32m\]\w\[\033[33m\]\$(parse_git_branch)\[\033[00m\] $ "
``` 

e Voilá

![Screenshot from 2022-11-19 21-03-30.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1668902629574/H_TmNEPB8.png align="left")

