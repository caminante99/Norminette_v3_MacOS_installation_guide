# Norminette V3 Installation Guide for MacOs users

Ce guide a pour vocation de vous aider à installer la Norminette V3 sur ce (foutu) MacOS\
DON'T PANIC AND FASTEN YOUR SEATBELT. 🛬

## Pourquoi ça ne fonctionne pas ? 

La Norminette V3 est écrite en Python3, donc lorsque que tu essayes de l'installer \
sur ton mac, celui-ci va essayer d'utiliser le Python3 pré-installé sur ton système \
qui est souvent :
1) Pas à jour
2) Non modifiable pour des raisons de sécurité

## La Solution : pyenv
Du coup, il existe deux méthodes, qui utilisent toutes les 2 le fabuleux gestionnaire de paquets pour MacOS : 🍺 Homebrew 🍺

Homebrew s'installe avec la commande :

```
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

L'une des méthodes est basée sur le téléchargement direct du python3.7 via `brew install python3.7`puis sur l'édition de ton PATH afin que le système chope le python de brew et non celui du système.

Pour notre méthode nous utiliserons plutôt **pyenv** qui est un gestionnaire d'environnement python. 

On télécharge pyenv via Homebrew : 
```
brew install pyenv
```

puis après cela on installe la version de python3 qui nous intéresse, ici la 3.7 :
```
pyenv install 3.7.9
```

La commande `pyenv versions` nous donne : 

![Capture d'écran](.img/Screenshot.png)

On fait :
```
pyenv global 3.7.9
```

et la commande `pyenv versions`nous donne cette fois : 

![Capture d'écran](.img/Screenshot2.png)