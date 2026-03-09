# TP 4 – Hibernate avec MySQL

## Description

Ce projet est une application Java utilisant **Hibernate** pour gérer la persistance des données dans une base de données **MySQL**.
Il permet de manipuler deux entités principales : **Salle** et **Machine**.

L’application implémente les opérations CRUD (Create, Read, Update, Delete) via une couche **DAO** et une couche **Service**.

---

## Technologies utilisées

* Java
* Hibernate ORM
* JPA (Java Persistence API)
* MySQL
* Maven
* JUnit (tests unitaires)

---

## Structure du projet

```
src
 ├── dao
 │    └── IDao.java
 │
 ├── entities
 │    ├── Machine.java
 │    └── Salle.java
 │
 ├── services
 │    ├── MachineService.java
 │    └── SalleService.java
 │
 ├── util
 │    └── HibernateUtil.java
 │
 └── test
      └── Test.java
```

---



Créer une base de données MySQL nommée :

```
tp4_db
```

Hibernate créera automatiquement les tables nécessaires.

---

## Entités

### Salle

Représente une salle contenant plusieurs machines.

Attributs :

* id
* code
* machines (liste de machines)

Relation :

* **OneToMany** avec Machine

### Machine

Représente une machine installée dans une salle.

Attributs :

* id
* ref
* dateAchat
* salle

Relation :

* **ManyToOne** avec Salle

---

## Fonctionnalités

Les services permettent de :

* Ajouter une salle ou une machine
* Modifier une salle ou une machine
* Supprimer une salle ou une machine
* Rechercher par identifiant
* Lister toutes les entités
* Rechercher les machines achetées entre deux dates

---

## Exécution du projet

1. Configurer la base de données MySQL.
2. Modifier le fichier `hibernate.cfg.xml`.
3. Lancer la classe :

```
test.Test
```

Cette classe :

* crée des salles
* ajoute des machines
* affiche les salles et leurs machines
* teste la recherche par date d’achat.

---

## Tests unitaires

Les tests sont réalisés avec **JUnit** pour vérifier les opérations CRUD :

* `SalleServiceTest`
* `MachineServiceTest`

Ces tests valident :

* création
* modification
* suppression
* récupération des données.

---

## Résultat

À l’exécution, Hibernate :

* crée automatiquement les tables
* insère les données
* exécute les requêtes SQL affichées dans la console.
  ---
<img width="1920" height="1080" alt="Screenshot (727)" src="https://github.com/user-attachments/assets/04d3a750-d043-445a-bd58-43f02480bcd8" />
<img width="1920" height="1080" alt="Screenshot (728)" src="https://github.com/user-attachments/assets/9ae6484f-3fb2-458a-929d-0bb7443a1aa0" />
<img width="1920" height="1080" alt="Screenshot (729)" src="https://github.com/user-attachments/assets/adf31dbd-92d0-41c1-adbb-e853156506af" />
<img width="1920" height="1080" alt="Screenshot (730)" src="https://github.com/user-attachments/assets/bd060ecd-2822-4617-8576-97e2542d0a48" />
<img width="1920" height="1080" alt="Screenshot (731)" src="https://github.com/user-attachments/assets/eb693ec8-2c7f-43a5-bb63-a4ff70e2a17e" />
<img width="1920" height="1080" alt="Screenshot (732)" src="https://github.com/user-attachments/assets/7f0190fc-fd9b-4a6e-b9af-7764a7d457ea" />
<img width="1920" height="1080" alt="Screenshot (733)" src="https://github.com/user-attachments/assets/6be147e9-5851-4dad-b5a6-02372f6dec66" />

---
# les tests
---
<img width="1920" height="1080" alt="Screenshot (736)" src="https://github.com/user-attachments/assets/6ac4959f-b47c-4b64-bb5e-721af9bfb96b" />
<img width="1920" height="1080" alt="Screenshot (737)" src="https://github.com/user-attachments/assets/08ee0d34-04fa-4ad5-b4eb-ebd8d8542f8a" />
<img width="1920" height="1080" alt="Screenshot (738)" src="https://github.com/user-attachments/assets/c88768e7-4a5b-4b68-93e3-a6ccc77f2383" />
<img width="1920" height="1080" alt="Screenshot (739)" src="https://github.com/user-attachments/assets/3a6dbc61-aa83-4b6c-a5ea-ccdc262b0743" />

<img width="1920" height="1080" alt="Screenshot (740)" src="https://github.com/user-attachments/assets/e9ca53c6-f875-4db3-bc44-9ec3b73bd7f2" />

<img width="1920" height="1080" alt="Screenshot (741)" src="https://github.com/user-attachments/assets/356313bc-9991-4367-a8d1-0726adfa6bf2" />


<img width="1920" height="1080" alt="Screenshot (742)" src="https://github.com/user-attachments/assets/ff3dcf46-88a4-4c06-a955-38939dc4b136" />

<img width="1920" height="1080" alt="Screenshot (743)" src="https://github.com/user-attachments/assets/05b35e50-b3aa-4079-83d2-1ac76aefc210" />
<img width="1920" height="1080" alt="Screenshot (744)" src="https://github.com/user-attachments/assets/b4fb05fc-93ee-466b-b7a6-e684028893f3" />


<img width="1920" height="1080" alt="Screenshot (745)" src="https://github.com/user-attachments/assets/011de056-f2b8-4880-b564-b0665a9114c1" />


<img width="1920" height="1080" alt="Screenshot (746)" src="https://github.com/user-attachments/assets/69380554-0869-4742-9158-22feff3cf6bb" />

<img width="1920" height="1080" alt="Screenshot (747)" src="https://github.com/user-attachments/assets/bbc4df1d-6d1e-4274-8bee-e300cadb7947" />

<img width="1920" height="1080" alt="Screenshot (748)" src="https://github.com/user-attachments/assets/b3a76fd6-430f-4393-b771-0e193a35af89" />

<img width="1920" height="1080" alt="Screenshot (749)" src="https://github.com/user-attachments/assets/fd730d64-6758-4676-8d98-d5cbe51ca465" />

<img width="1920" height="1080" alt="Screenshot (750)" src="https://github.com/user-attachments/assets/3da66403-4484-47be-bd2a-8ac6d420340d" />


<img width="1920" height="1080" alt="Screenshot (751)" src="https://github.com/user-attachments/assets/88b0046a-b5a9-4e7e-afe0-fb8a34995c06" />


<img width="1920" height="1080" alt="Screenshot (752)" src="https://github.com/user-attachments/assets/3cf6b40d-26c1-4da9-95ac-432e7ea35fb1" />

<img width="1920" height="1080" alt="Screenshot (753)" src="https://github.com/user-attachments/assets/6e27a29f-c29c-48b0-9d08-a5232c53f619" />


<img width="1920" height="1080" alt="Screenshot (754)" src="https://github.com/user-attachments/assets/b7c6dd32-60de-4b63-8d6b-d94a5fe41cda" />


<img width="1920" height="1080" alt="Screenshot (755)" src="https://github.com/user-attachments/assets/be97a534-5e0b-472d-849b-bad35fa3d0e9" />

<img width="1920" height="1080" alt="Screenshot (756)" src="https://github.com/user-attachments/assets/afcbbb2e-9004-4a62-9219-bfcef5b85cb8" />

<img width="1920" height="1080" alt="Screenshot (757)" src="https://github.com/user-attachments/assets/eb0c262d-0529-44f1-accd-4276d2aa908d" />
<img width="1920" height="1080" alt="Screenshot (758)" src="https://github.com/user-attachments/assets/756fe7d5-bcc5-4865-907b-17f3bd29df6e" />

<img width="1920" height="1080" alt="Screenshot (759)" src="https://github.com/user-attachments/assets/982d96e5-78ba-459a-80a6-8d9951c25685" />

<img width="1920" height="1080" alt="Screenshot (760)" src="https://github.com/user-attachments/assets/9b358649-fb06-4b07-872e-3a81e6305e5b" />
<img width="1920" height="1080" alt="Screenshot (761)" src="https://github.com/user-attachments/assets/8bc1f272-3c30-46dc-a8c3-2d0f0a907a85" />
<img width="1920" height="1080" alt="Screenshot (762)" src="https://github.com/user-attachments/assets/74042590-b0ba-432d-9f9c-7e57cc2d791d" />

---

## Auteur

TP réalisé dans le cadre du module **Développement JakartaEE / Hibernate**.
