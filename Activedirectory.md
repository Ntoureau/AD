# **Installation d'Active Directory sur Windows Server**
Ouvrir le gestionnaire de serveur et sélectionner "Ajouter des rôles et des fonctionnalités" puis dans l'onglet "Rôles de Serveur" cocher "Services AD DS" (Active Directory Domain Services) et valider les fonctionnalités complémentaires.

![01activedirectory.png](https://github.com/Ntoureau/imagesAD/blob/main/Active%20Directory/01activedirectory.png?raw=true)

Cliquer sur Suivant et enfin "Installer"

Une fois l'installation terminée, sélectionner "Promouvoir ce serveur en contrôleur de domaine", ou fermer puis cliquer sur la notification de l'onglet "Gérer".

![02promouvoircontroleurdomaine.png](https://github.com/Ntoureau/imagesAD/blob/main/Active%20Directory/02promouvoircontroleurdomaine.png?raw=true)

Choisir "Ajouter une nouvelle forêt" et définir un nom de domaine racine (ex : wilder.lan)

![03nomdomaineracine.png](https://github.com/Ntoureau/imagesAD/blob/main/Active%20Directory/03nomdomaineracine.png?raw=true)

Si tous les postes sont sous Windows 10, on laisse les niveaux fonctionnels par défaut (Windows Server 2016), sinon il faut baisser le niveau fonctionnel à leur équivalent.
On laisse cocher le Serveur DNS et on définit un mot de passe global (ex : wild10)

![04optioncontroleurdomaine.png](https://github.com/Ntoureau/imagesAD/blob/main/Active%20Directory/04optioncontroleurdomaine.png?raw=true)

On définit ensuite le nom de domaine NetBIOS (cela influera sur les appareils ne gérant pas les noms de domaine qualifiés, ici WILDER).
On valide ensuite les emplacements de la base de données Active Directory (ici le chemin par défaut).

![05cheminpardefaut.png](https://github.com/Ntoureau/imagesAD/blob/main/Active%20Directory/05cheminpardefaut.png?raw=true)

Cliquer sur suivant pour vérifier la configuration requise, puis cliquer sur Installer.

Désormais la connexion se fait sur le domaine pour utiliser le compte Administrateur.

![06connexion.png](https://github.com/Ntoureau/imagesAD/blob/main/Active%20Directory/06connexion.png?raw=true)

# **Création des comptes utilisateurs du domaine**
Avant d'ajouter de nouveaux postes au réseau, il faut ajouter les comptes pour les utilisateurs du domaine.
Sélectionner "Outils" et choisir "Utilisateurs et ordinateurs Active Directory"

![07creerutilisateurs.png](https://github.com/Ntoureau/imagesAD/blob/main/Active%20Directory/07creerutilisateurs.png?raw=true)

Faire un clic droit sur le nom du domaine et sélectionner "Nouveau" > "Unité d'organisation" et lui donner un nom (ex : Wilders)

![08uniteorganisation.png](https://github.com/Ntoureau/imagesAD/blob/main/Active%20Directory/08uniteorganisation.png?raw=true)

Faire un clic droit sur l'unité d'organisation créée, "Nouveau" > "Utilisateur"

![09nouveaututilisateur.png](https://github.com/Ntoureau/imagesAD/blob/main/Active%20Directory/09nouveautuilisateur.png?raw=true)

Renseigner le Prénom, le Nom et Nom d'ouverture de session et préciser ensuite un mot de passe avec la condition voulue.

![10choixnom.png](https://github.com/Ntoureau/imagesAD/blob/main/Active%20Directory/10choixnom.png?raw=true)

Le serveur est désormais installé et opérationnel. 