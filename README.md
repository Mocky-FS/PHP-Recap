# PHP Synthèse

## Sommaire

- [Classe Abstraite](#classe-abstraite)

## Classe Abstraite

```php
<pre>
<?php

// Classe abstraite Vehicule
abstract class Vehicule {
    // Propriétés
    protected $marque;
    protected $modele;
    protected $nbRoues;

    // Méthode abstraite
    abstract public function rouler();

    // Méthode concrète
    public function afficherInfos() {
        echo "Marque : " . $this->marque . "<br>";
        echo "Modèle : " . $this->modele . "<br>";
        echo "Nombre de roues : " . $this->nbRoues . "<br>";
    }
}

// Classe Voiture qui hérite de la classe abstraite Vehicule
class Voiture extends Vehicule {
    // Implémentation de la méthode abstraite rouler()
    public function rouler() {
        echo "La voiture roule sur 4 roues<br>";
    }
}

// Interface Roues
interface Roues {
    // Méthode rouler()
    public function rouler();
}

// Classe Moto qui implémente l'interface Roues
class Moto implements Roues {
    // Implémentation de la méthode rouler()
    public function rouler() {
        echo "La moto roule sur 2 roues<br>";
    }
}

// Instanciation d'un objet Voiture
$voiture = new Voiture();
$voiture->marque = "Peugeot";
$voiture->modele = "208";
$voiture->nbRoues = 4;
$voiture->afficherInfos();
$voiture->rouler();

// Instanciation d'un objet Moto
$moto = new Moto();

```


Chapitre 1 : Les structures de contrôle
Chapitre 2 : Les Fonctions
Chapitre 3 : Les tableaux
Chapitre 4 : Introduction à HTTP avec PHP
Chapitre 5 : Les formulaires 
Chapitre 6 : Le système de fichiers avec PHP
Chapitre 7 : Les cookies et les sessions
Chapitre 8 : les dates
Chapitre 9 : Programmation orientée objet & Dynamisation
Chapitre 10 : les namespaces
Chapitre 11 : La gestion d'erreur
Chapitre 12 : Introduction à MySQL
Chapitre 13 : Utiliser une base de données avec PDO
Chapitre 14 : Composer et autoload
Chapitre 15 : Authentification avec les sessions
Chapitre 16 : Configuration d'un serveur Web de production avec Nginx