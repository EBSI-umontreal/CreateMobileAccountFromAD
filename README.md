# CreateMobileAccountFromAD

Ce script permet d'automatiser la création de profils mobiles pour des groupes Active Directory sur des postes Mac liés à un domaine.
En effet, si l'utilisatrice ou l'utilisateur ne possède pas de profil sur un poste Mac, il ne lui sera pas possible de se connecter via la fonction "Partage d'écran" native de l'OS, ce qui peut être une limitation importante lors de la mise en place d'un laboratoire virtuel Mac.

# Utilisation

Le script doit être exécuté depuis un poste Windows relié au domaine. Celui-ci produira des scripts Shell à exécuter sur les postes Mac pour créer  les comptes mobiles en lot.

Plus précisément :

1. Éditez le script pour modifier l’OU et les groupes AD d’usagers à inclure (sous la ligne `'GROUPES A INCLURE` ).

2. Double-cliquez sur le fichier du script pour l’exécuter à partir d’un poste Windows du domaine.
   Celui-ci va produire un fichier `createProfil.command` (script SH pour créer les profils) et `deleteProfil.command` (pour faire l’inverse, au besoin).

3. Depuis le poste Mac, exécutez le script généré :
   `chmod +x createProfil.command`
   `./createProfil.command`

# Licence

https://creativecommons.org/licenses/by-nc/4.0/