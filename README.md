#ORM-r
=====

Information:
------------

* Compatibilité mySQL
* Terminal de commaande afin d'aider l'utilisateur (php orm/console/console.php)
* Une gestion des logs est possible (pensez a avoir un dossier log à la racine du projet)
* La base de donnée peut Être crée via une commande, mais les tables doivent être faite manuellement
* Possibilitée de supprimer toute la base de données

Installation:
-------------

* Placez le dossier orm à la ressource de votre projet
* Configurez les informations de la base de données dans config/conf.php

Utilisation:
------------

* A mettre au début du votre fichier:
    require_once "./orm/Entity/orm.php";
    require_once "config/conf.php";
* Instanciez la class avec $myVar = new ORM($config);
* Appelez les différentes méthodes afin d'utiliser l'ORM

Liste des fonctions:
--------------------

* public function execQuery($query)
    -> Permet d'éxécuter une requette mySQL
* public function select($table, $fields = "*", $where = "", $order = "", $limit = "")
    -> Permet de selectionner ce que l'on souhaite
* public function insert($table, $fields, $values)
    -> Permet l'insertion de données
* public function update($table, $fields, $values, $where = "")
    -> Modification d'une donnée
* public function remove($table, $where = "")
    -> Suppression d'une donnée
* public function find($table, $id)
    -> Permet de récupérer suivant un id
* public function findAll($table)
    -> Permet de tout récupérer
* public function findBy($table, $field, $value)
    -> Permet de sélectionner des éléments selon le type souhaité
* public function findOneBy($table, $field, $value)
    -> Permet de séléctionner un seul élément selon le type souhaité
* public function count($table, $row = "*", $where = "")
    -> Comptage sans sélection d'après une requête donnée
* public function check($table, $row, $where = "")
    -> Permet de vérifier l'existence d'une donnée
