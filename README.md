# postgresql_intallation
https://www.enterprisedb.com/downloads/postgres-postgresql-downloads
![postgreSQL](xpostgresql.jpg.pagespeed.ic.82ZZ05AnGg.jpg)

```
L'installation de PostgreSQL sur un système Windows, n'est pas forcement aisée. Ce guide vous aidera à contourné toutes difficultés.
```


1. Désinstaller PostgreSQL  (si vous avez fait une installation qui a échoué)

#### Ouvrir l'invite de commande puis excecuter 
2. Supprimer l'utilisateur postgres s'il existe 
```
net user postgres /delete   
```
3. Créer un nouvelle utilisateur postgres avec mot de passe
```
net user /add postgres <password>
```
4. Ajouter l'utilisateur postgres au groupe Administrateurs
```
net localgroup administrators postgres /add
```
ou (pour une installation de windows en français)
```
net localgroup administrateurs postgres /add
```
5. Ajouter l'utilisateur postgres au groupe Utilisateurs avec pouvoir

```
net localgroup "power users" postgres /add
```
ou  (pour une installation de windows en français)
```
net localgroup "Utilisateurs avec pouvoir" postgres /add
```
6. Exécutez une fenêtre de commande en tant qu'utilisateur postgres

```
runas /user:postgres cmd.exe
```
7. Exécutez le fichier d'installation à partir de la fenêtre de commande.

```
C:\Download\name_of_postgres_intaller
```

si le fichier n'est pas retrouvénou que vous n'avez pas le droit d'accès, Copier et coller  l'intallable de postgres dans le dossier téléchargements ou download de l'utilisateur postgres

**NB**: Je vous conseille de choisir comme **langue d'installation l'anglais**. je n'ai aucune assurance que l'installation se deroule bien pour tout autre langue

8. Supprimez l'utilisateur postgres du groupe Administrateurs.
```
net localgroup administrators postgres /delete
```
ou 
```
net localgroup administrateurs postgres /delete
```

Source:
https://dba.stackexchange.com/questions/10241/postgresql-the-database-cluster-initialization-failed?answertab=active#

```
vous pouvez aussi supprimer l'utilisateur postgres de votre pc en suivant ce guide
https://winaero.com/blog/delete-user-profile-windows-10/
```

https://winaero.com/blog/delete-user-profile-windows-10/


##### Vérifier si postgres est installé

Cliquer sur le boutton windows, dans la liste des programmes, vous trouverez le dossier d'installation de postgres, à l'intérieur faites un clique sur le fichier SQL shell.


![shell](shell.png)

Dans la console qui s'affichera, laisser les infos par défaut.


![shell_log](shell_log.png)

