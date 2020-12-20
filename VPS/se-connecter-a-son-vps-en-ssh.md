Dans un premier temps, nous allons installer un logiciel nous permettant de nous connecter en SSH, dans ce guide, nous utiliserons [PUTTY](https://the.earth.li/~sgtatham/putty/latest/w64/putty-64bit-0.74-installer.msi). Une fois installé, lancez le !

![](https://gblobscdn.gitbook.com/assets%2F-MD7IL6lJMQPqWCnSSXr%2F-MDLllaJ8FqFgiCitx-c%2F-MDLq24WjsqI60khAu6Y%2Fview_putty.png?alt=media&token=2e76347c-989b-47f8-889c-52d8ca972a85)

Nous allons pouvoir maintenant nous connecter, dans un premier temps, assurez-vous d'être en possession de l'ip de votre serveur, de l'utilisateur, du mot de passe et du port.
Dans la partie "Host Name (or IP address) indiquez l'adresse IP de votre serveur.

Dans la partie "Port" assurez-vous d'avoir bien le port 22 et dans la partie "Connection type" vérifiez que "SSH" est bien coché.

Si tout est bon, cliquez sur "Open" ; Nous allons ouvrir une session SSH !

Si vous recevez une alerte de sécurité tel que "The server's host key is not cached in the registry (...)" cliquez simplement sur "Oui".

Il va maintenant vous demander le nom de votre utilisateur pour ouvrir la session SSH dans notre cas il s'agit de l'utilisateur `root`.

![](https://gblobscdn.gitbook.com/assets%2F-MD7IL6lJMQPqWCnSSXr%2F-MDLllaJ8FqFgiCitx-c%2F-MDLsctwFJ6Jzfd7nbtN%2Fview_putty_login.png?alt=media&token=1e47254d-4394-4229-a012-84c116f2ae59)

Une fois que vous avez inscrit votre utilisateur, cliquez sur votre touche "Entrée" puis il va vous demander le mot de passe, si vous souhaitez le copier / coller, il faut savoir que ctrl + c / ctrl + v le fonctionne pas il faut faire un clic droit avec sa souris pour le coller après l'avoir copié. Si comme dans notre cas vous l'inscrivez manuellement rassurez-vous tout de suite c'est normal que vous ne voyez aucune lettre / chiffre s'inscrire de même lorsque vous collez le mot de passe, c'est une sécurité !

![](https://gblobscdn.gitbook.com/assets%2F-MD7IL6lJMQPqWCnSSXr%2F-MDLllaJ8FqFgiCitx-c%2F-MDLtSwvt0TH-CchXf72%2Fview_putty_login_password.png?alt=media&token=13153c58-942e-4589-a174-9334e2e5d130)

Une fois le mot de passe inscrit, cliquez encore une fois sur "Entrée" et voilà vous venez d'ouvrir une session en SSH sur votre serveur VPS !

![](https://gblobscdn.gitbook.com/assets%2F-MD7IL6lJMQPqWCnSSXr%2F-MDLllaJ8FqFgiCitx-c%2F-MDLtcSKseh_1CxW2ksB%2Fview_putty_ssh.png?alt=media&token=c26380ce-1fc8-4055-89c2-49e1a755d96d)

Nous vous invitons désormais à sécuriser celui-ci en suivant [ce tutoriel](https://wiki.world-heberg.com/base-de-connaissances-vps/bien-securiser-son-vps).
