# Weblate pour YunoHost

[![Niveau d'intégration](https://dash.yunohost.org/integration/weblate.svg)](https://dash.yunohost.org/appci/app/weblate) ![](https://ci-apps.yunohost.org/ci/badges/weblate.status.svg) ![](https://ci-apps.yunohost.org/ci/badges/weblate.maintain.svg)  
[![Installer Weblate avec YunoHost](https://install-app.yunohost.org/install-with-yunohost.svg)](https://install-app.yunohost.org/?app=weblate)

*[Read this readme in english.](./README.md)*
*[Lire ce readme en français.](./README_fr.md)*

> *Ce package vous permet d'installer Weblate rapidement et simplement sur un serveur YunoHost.
Si vous n'avez pas YunoHost, regardez [ici](https://yunohost.org/#/install) pour savoir comment l'installer et en profiter.*

## Vue d'ensemble

Weblate est un outil de traduction libre avec une intégration étroite du contrôle de version. Il fournit deux interfaces utilisateur, la propagation des traductions entre les composants, les contrôles de qualité et la liaison automatique aux fichiers source. 

**Version incluse :** 4.11.2~ynh2

**Démo :** https://hosted.weblate.org/

## Captures d'écran

![](./doc/screenshots/BigScreenshot.png)

## Avertissements / informations importantes

## GitHub

Vous devrez donner à Weblate un utilisateur GitHub et un jeton. Veuillez lire [la documentation de GitHub sur le jeton](https://help.github.com/articles/creating-a-personal-access-token-for-the-command-line/).
Cet utilisateur ne sera utilisé que pour ouvrir la pull-request, chaque traduction garde son auteur.

**Clés SSH**, vous devrez vous rendre dans l'administration, générer une clé publique pour Weblate et ajouter github.com pour que Weblate connaisse l'empreinte digitale. Veuillez noter que si votre compte possède déjà une clé publique (ssh-rsa), vous devrez ajouter manuellement celle de Weblate à votre compte GitHub.

## Paramètres et mises à niveau

Presque tout ce qui concerne la configuration de Weblate est géré dans un fichier `settings.py`.
Vous pouvez éditer le fichier `$final_path/local_settings.py` pour activer ou désactiver des fonctionnalités.

# Divers

## Connexion LDAP

Cela ne fonctionne pas encore, mais bien que [cela semble faisable](https://docs.weblate.org/en/latest/admin/auth.html?highlight=LDAP#ldap-authentication), je ne suis pas sûr que ce soit le cas une bonne idée de connecter ce genre d'outils à votre LDAP. 
## Documentations et ressources

* Site officiel de l'app : https://weblate.org
* Documentation officielle utilisateur : https://docs.weblate.org/
* Documentation officielle de l'admin : https://docs.weblate.org/
* Dépôt de code officiel de l'app : https://github.com/WeblateOrg/weblate
* Documentation YunoHost pour cette app : https://yunohost.org/app_weblate
* Signaler un bug : https://github.com/YunoHost-Apps/weblate_ynh/issues

## Informations pour les développeurs

Merci de faire vos pull request sur la [branche testing](https://github.com/YunoHost-Apps/weblate_ynh/tree/testing).

Pour essayer la branche testing, procédez comme suit.
```
sudo yunohost app install https://github.com/YunoHost-Apps/weblate_ynh/tree/testing --debug
ou
sudo yunohost app upgrade weblate -u https://github.com/YunoHost-Apps/weblate_ynh/tree/testing --debug
```

**Plus d'infos sur le packaging d'applications :** https://yunohost.org/packaging_apps