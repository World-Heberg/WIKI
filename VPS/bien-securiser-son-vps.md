Avant toutes choses, il faut mettre à jour le serveur à l'aide des commandes suivantes :

```
apt-get update
apt-get upgrade
```

Il est fortement conseillé de mettre à jour son VPS toutes les semaines afin de garder les composants à jour.

Dans un premier temps, nous allons comment voir pour changer votre port de connexion SSH (qui par défaut est 22).

```
nano /etc/ssh/sshd_config
```

Une fois cette commande effectuée, cherchez la ligne suivante dans le fichier (en naviguant les flèches du haut et du bas) :

```
Port 22
```

À présent, il vous suffit de modifier 22 par le nouveau port SSH de connexion souhaité. 

Attention : il est possible que cette ligne dispose d'un hastag (#) devant. Dans ce cas là, il vous suffit de le retirer pour enlever le mode « commentaire » de cette ligne.

Une fois cette modification effectué, faites CTRL + O suivi de la touche Entrer afin de sauvegarder les modifications. Pour quitter l'édition du fichier de configuration, faites CTRL + X !

Afin de valider l'intégralité de ses changements, nous devons effectuer un redémarrage SSH de la machine. Pour ce faire, exécuter la commande suivante :

```
/etc/init.d/sshd restart
```

Une fois le redémarrage SSH de la machine effectué, reconnectez-vous à votre machine avec votre nouveau port SSH de connexion choisi lors de la modification de celui-ci.

Félicitation ! Vous venez désormais de changer votre port SSH de votre machine pour plus de sécurité.

Dans un second temps, **il est fortement recommandé d'utiliser un autre utilisateur que root pour se connecter à votre machine**. Nous allons donc à présent voir comment créer un utilisateur linux avec des droits restreint et qui puisse agir dans le système avec des droits root.

Pour commencer, nous allons créer un utilisateur avec la commande suivante :

```
adduser tutoriel
```

Pour ma part, j'ai choisi d'appeler mon utilisateur **tutoriel** mais vous êtes totalement libre de choisir celui que vous souhaitez.

Une fois cette commande effectuée, on vous demandera de choisir un mot de passe sécurisé pour mettre la connexion à votre machine depuis ce compte.

Si vous êtes connecté à ce compte et que vous souhaitez effectuer des actions d'administrations au sein de votre machine. Effectuez la commande suivante :

```
su root
```

Vous devrez ensuite indiquer le mot de passe associé à l'utilisateur root pour valider.

Parfait ! Vous venez à présent de créer un utilisateur ayant des droits restreints au sein de votre machine.

Il est très dangereux de laisser votre VPS accessible uniquement depuis l'utilisateur root, car ce compte peut effectuer certaines opérations qui seront irréversibles sur votre serveur. À présent, nous allons voir comment désactiver la connexion avec l'utilisateur root au sein de votre machine.

Pour se faire, nous devons nous rendre dans les paramètres de configuration SSH à l'aide de la commande suivante :

```
nano /etc/ssh/sshd_config
```

Une fois ceci effectué, chercher la ligne suivante au sein du fichier de configuration :

```
PermitRootLogin yes 
```

Il vous suffit à présent de remplacer **yes** par **no** pour empêcher l'utilisateur root de se connecter. 

Attention : il est possible que cette ligne dispose d'un hastag (#) devant. Dans ce cas là, il vous suffit de le retirer pour enlever le mode « commentaire » de cette ligne.

À présent, nous devons redémarrer le service SSH afin que nos modifications soit bien prise en compte :

```
/etc/init.d/ssh restart
```

Parfait ! Vous venez à présent d'interdire le fait que l'utilisateur root puisse se connecter à votre machine.

À présent, nous allons voir un dernier point pour bien sécuriser votre VPS : l'installation et la configuration du paquet fail2ban.

Afin d'installer le package logiciel, effectuez la commande suivante :

```
apt-get install fail2ban
```

Une fois que le paquet est bien installé, il faut modifier le fichier de configuration à votre guise afin qu'il soit adapter à vous. Cependant, il est recommandé de faire une sauvegarde du fichier de configuration à l'aide de la commande suivante :

```
cp /etc/fail2ban/jail.conf /etc/fail2ban/jail.conf.backup
```

Parfait ! Maintenant vous pouvez configurer les paramètres du paquet à l'aide de la commande suivante :

```
nano /etc/fail2ban/jail.conf
```

Une fois que vous avez bien configuré comme vous le souhaitiez, il faut redémarrer le service pour prendre en compte les changements apportés :

```
/etc/init.d/fail2ban restart
```

Nous avons enfin terminé ce tutoriel au sein de la base de connaissance. Vous venez d'installer le paquet fail2ban avec succès et votre machine devrait être bien sécurisé.
