# PHP Synthèse

## Sommaire

- [Classe Abstraite](#classe-abstraite)

## Classe Abstraite

```php
<?php
echo "<pre>";


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
