# course-php-legacy-code

- Pour linter en modifiant le code 

- Pour linter le php sans modifications

```docker run -v $PWD:/app phpqa/php-cs-fixer fix --dry-run www```

-----

1/ Fork https://github.com/cgrandval/cours-legacy/tree/main/www
2/ Cloner votre repository forké
3/ Installez le / lancez-le

- si docker : docker-compose up -d
- http://localhost si port already bind alors changer le port ligne 6
- si pas docker, les sources sont dans www et le sql de la base dans sql (il faut créer la base avant)

4/ Appliquer phpcs-fixer au code https://hub.docker.com/r/phpqa/php-cs-fixer
```docker run -v $PWD:/app phpqa/php-cs-fixer fix --dry-run www```
- Si pas docker https://github.com/FriendsOfPHP/PHP-CS-Fixer
  
  https://github.com/FriendsOfPHP/PHP-CS-Fixer/blob/2.17/doc/installation.rst

5/ Corriger le docker-compose.yml, ligne 22, remplacer ./import.sql par ./sql/import.sql -> faites une branche, modifier, git add, commit, push