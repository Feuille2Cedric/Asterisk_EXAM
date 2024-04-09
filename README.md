# Commande Exam Asterisk

où on trouve les fichiers anglais et français : `/var/lib/asterisk/sound/en` et `/var/lib/asterisk/sound/fr`


Compter le nombre de fichiers au total : 

```bash
find /var/lib/asterisk/sounds/en | wc -l (-l = nombre de lignes)
```

Compter le nombre de fichier d'un certain type :

```bash
find /var/lib/asterisk/sounds/en -name "*.gsm" | wc -l 
```

Donner tous les types de fichiers dans un dossier :

```bash
find /chemin/vers/votre/dossier -type f -exec sh -c 'echo "${0##*.}"' {} \; | sort | uniq
```
