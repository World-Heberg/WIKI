Bonjour et bienvenue dans ce nouvel article de notre WIKI.
Dans cet article, nous allons vous montrer comment vous connecter à votre VPS via le protocole SSH.

Dans un premier temps, il vous faudra installer le logiciel Putty que vous pourrez trouver [ici](https://www.chiark.greenend.org.uk/~sgtatham/putty/latest.html). Nous vous recommandons d'installer la version .exe de ce logiciel.

Une fois celà fait, vous devrez lancer le logiciel que vous venez d'installer. Un écran comme celui ci-dessous apparaît :

<img src="https://i.ibb.co/GFsgVF4/putty-init.png" alt="putty-init">

Vous allez maintenant pouvoir vous connecter à votre VPS. Vous aurez besoin, pour ce faire, de l'adresse ip de votre VPS ainsi que du nom d'utilisateur et du mot de passe de celui-ci. Ces identifiants vous ont étés envoyés par e-mail, une fois votre VPS livré.

Dans le champ "Host Name (or IP adress), vous allez pouvoir insérer l'adresse ip v4 de votre vps, vous devrez également vérifier que le port est bien le port 22 ainsi que la case cochée dans la partie "Connection type" est bien SSH. Si tout celà est bon, vous allez maintenant pouvoir cliquer sur le bouton "Open".

Après avoir cliqué sur "Open", il se peut que vous receviez une alerte comme celle-ci :

<img src="https://i.ibb.co/3YJsCL8/putty-alert.png" alt="putty-alert">

Ne vous inquiétez pas, rien de grave. Il vous suffit simplement de cliquer sur "Oui".

Une fois ceci fait, nous allons pouvoir nous connecter à notre VPS. Vous allez donc devoir, dans un premier temps, entrer l'identifiant, dans notre cas, `root`

<img src="https://i.ibb.co/Dk0tvtp/putty-username.png" alt="putty-username" border="0">

Une fois celui-ci inscrit, vous allez pouvoir appuyer sur la touche "Entrée" de votre clavier. 

Vous allez ensuite, pouvoir entrer votre mot de passe.

<img src="https://i.ibb.co/PC1ynvP/putty-password.png" alt="putty-password">

**Attention :** - Lors de la saisie de celui-ci, il est normal qu'aucun caractère ne s'affiche. Ceci est une sécurité de Putty.
                - Si vous voulez copier/coller le mot de passe, le contrôle clavier `CTRL+C` ne **fonctionne pas**. Vous devrez sois utiliser la souris et faire un clique droit                     puis cliquer sur coller, sois utiliser le contrôle clavier `MAJ+INSER`. Il est également normal, lors du copié/collé qu'aucun caractère ne s'affiche.
                
Une fois le mot de passe saisi, vous allez maintenant pouvoir appuyer à nouveau sur la touche "Entrée".

**Félicitations !** Vous avez maintenant ouvert une session SSH sur votre VPS !
<img src="https://i.ibb.co/NZfyN2r/putty-login.png" alt="putty-login">
