#ORM-r
=====

Information:
------------

* Compatibilit� mySQL
* Terminal de commaande afin d'aider l'utilisateur (php orm/console/console.php)
* Une gestion des logs est possibles(pensez a avoir un dossier log � la racine du projet)
* La base de donn�e peut �tre cr�e via une commande, mais les tables doivent �tre faite manuellement
* Possibilit� de supprim� toute la base de donn�e

Installation:
-------------

* Placer le dossier orm � la ressource de votre projet
* Configurer les informations de la base de donn�e dans config/conf.php

Utilisation:
------------

* A mettre au d�but du votre fichier:
    require_once "./orm/Entity/orm.php";
    require_once "config/conf.php";
* Instancier la class avec $myVar = new ORM($config);
* Appeler les diff�rentes m�thodes afin d'utiliser l'ORM

Liste des fonctions:
--------------------

* public function execQuery($query)
    -> Permet d'�x�cuter une requette mySQL
* public function select($table, $fields = "*", $where = "", $order = "", $limit = "")
    -> Permet de selectionner ce que l'on souhaite
* public function insert($table, $fields, $values)
    -> Permet l'nsertion de donn�e
* public function update($table, $fields, $values, $where = "")
    -> Modification d'une donn�e
* public function remove($table, $where = "")
    -> Suppr�tion d'une donn�e
* public function find($table, $id)
    -> Permet de r�cup�r� suivant un id
* public function findAll($table)
    -> Permet de tout r�cup�r�
* public function findBy($table, $field, $value)
    -> Permet de s�l�ctionn� des �l�ments selon le type souhait�
* public function findOneBy($table, $field, $value)
    -> Permet de s�l�ctionn� un seul �l�ment selon le type souhait�
* public function count($table, $row = "*", $where = "")
    -> Comptage sans s�lection d'apr�s une requ�te donn�e
* public function check($table, $row, $where = "")
    -> Permet de v�rifier l'existence d'une donn�e
