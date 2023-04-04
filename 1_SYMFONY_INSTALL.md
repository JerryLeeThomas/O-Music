# 1 - Installation Symfony dans le projet

## Symfony skeleton (sans webapp)

<https://symfony.com/doc/current/setup.html>

    composer create-project symfony/skeleton:"^5.4" nom_du_projet

## Ajout des annotations
  
<https://symfony.com/doc/5.4/page_creation.html#annotation-routes>

    composer require annotations

## Ajout du Profiler

<https://symfony.com/doc/5.4/profiler.html>

    composer require --dev symfony/profiler-pack

## Ajout de Twig

<https://twig.symfony.com/doc/3.x/installation.html>

    composer require "twig/twig:^3.0"

## Ajout de Doctrine ORM + Maker

<https://symfony.com/doc/current/doctrine.html>

    composer require symfony/orm-pack
    composer require --dev symfony/maker-bundle

## Ajouts utilitaires à la main dans le projet

- Dans ```settings.json```, accès via le raccourci : **ctrl+maj+p** puis taper **settings.json** et enfin cliquer sur **paramètres d'espace de travail**. Le code ajouté s'occupe de la gestion de l'autocompletion html dans les docs JS, Vue et Twig. ```settings.json``` ce trouvera ensuite dans le dossier ```.vscode``` à la racine de notre projet. Code à ajouter :

```json
    {
    "emmet.includeLanguages": 
        {
        "javascript": "javascriptreact",
        "vue-html": "html",
        "twig": "html"
        }
    }
```

- Dans ```twig```, accès via le chemin : **config>packages>twig.yaml**. Le code ajouté permet de bien utiliser le Framework Bootstrap dans nos templates twig. Code à ajouter :

```yaml
    form_themes: ["bootstrap_5_layout.html.twig"]
```

- Dans ```Framework: default local:```, accès via le chemin : **config>packages>translation.yaml**. Taper ```fr``` en remplacement de ```en```

- Dans ```Framework:```, accès via le chemin :  **config>packages>framework.yaml**. Décommentér la ligne ```csrf_protection: true``` pour mettre automatiquement les tokens sur les formulaires:

```yaml
    # csrf_protection: true

    to
    
    csrf_protection: true
```
