# Jlailu

## Installation

### JBoss

Installer `wildfly`, puis pour pouvoir le lancer sans sudo il faut s'ajouter au groupe `wildfly` :
```bash
sudo usermod -aG wildfly $USER
sudo chmod g+rw -R /opt/wildfly
```

Après s'être déloguer puis reloguer, tester que `/opt/wildfly/bin/standalone.sh` se lance sans erreur.

### Intellij-idea

Après avoir cloné le repo, il faut ouvrir le dossier `jlailu` dans intellij-idea (version ultimate).
```bash
git clone git@git.inpt.fr:pillott/jlailu.git
```
Il y a déjà une configuration nommée `JBoss` installée. Il faut l'éditer et changer `Application server` pour qu'il pointe
vers `/opt/wildly`.

Lancez cette configuration et allez sur [http://localhost:8080/backend/api/hello-world](http://localhost:8080/backend/api/hello-world),
si ça fonctionne vous devez voir `Hello, World!`.

