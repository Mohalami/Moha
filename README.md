# Mohamed Lamine

Ce site est un projet de m formtion CCi qui presentera des oeuvres que l'on peut visiter commenter et ajouter aux favoris.

## Environnement de developpement

## Pre-requis

*PHP 7.4 min
*Composer
*Symfony CLI
*Docker
*Docker-compose

Vous pouvez verifier les pre-requis (sauf Docker et Docker-compose) avec la commande suivante (de la CLI Symfony):

```bash
symfony check:requirements
```

### Lancer l'environnement de developpement 

```bash
composer install
docker-compose up -d
symfony serve -d
```

### Ajouter des donnees de tests
```bash
symfony console doctrine:fixtures:load

### Lancer les test 
```bash
php bin/phpunit --testdox
```

###mis de cote car casse le code mais pourra etre revisiter, a inserer dans realisation.twig juste apres la fermeture de la derniere div avant de fermer la section Ce code sert a faire fonvtionner la pagination
<!--  <div>
            {%do peinture.setPageRange(2) %}
            {{ knp_pagination_render(peintures, 'base/pagination.html.twig') }}
        </div> -->

## Production
### envoie des mails de contacts
Les mails de prise de contact sont stockés en bdd, pour les envoyer au peintre par mail, il faaut mettre en place un cron sur: 
```bash
symfony console app:send-contact
```