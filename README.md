# Dépôt de paquets FKM

Ce dépôt contient **uniquement les paquets pacman** de FKM (Free Kernel Machine), une distribution
basée sur Arch Linux avec le bureau KDE Plasma. Il ne contient pas de code source : il sert de
serveur de paquets pour `pacman`.

## Les canaux

| Canal | Pour qui | Adresse |
|---|---|---|
| `stable` | Les installations FKM | `https://github.com/NearFKM/fkm-depot/releases/download/stable` |
| `test` | Les machines de test | `https://github.com/NearFKM/fkm-depot/releases/download/test` |

Une version passe de `test` à `stable` sans être reconstruite : ce sont exactement les fichiers testés.
Le canal `stable` reste vide jusqu'à la première version officielle de FKM.

## Dans pacman.conf

L'installateur FKM l'ajoute tout seul :

```
[fkm]
SigLevel = Required DatabaseRequired
Server = https://github.com/NearFKM/fkm-depot/releases/download/stable
```

## Signature

Tous les paquets et la base du dépôt sont signés par la clé FKM, que le paquet `fkm-keyring`
ajoute au trousseau de pacman. pacman refuse tout paquet FKM non signé ou modifié.

- Identité : `FKM (signature des paquets) <nearfkm@proton.me>`
- Empreinte : `12608CD53C9EFB53000B48C67129A4F6D212F594`
