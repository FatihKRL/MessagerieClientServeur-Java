# SAE - Objets Communicants 🚀

## Description du projet 📝

Ce projet a pour objectif de créer une **application client-serveur en Java** permettant la gestion d'un réseau social simple, avec des échanges de messages en temps réel ou en mode boîte à lettres 📩. L'application utilise des **sockets TCP/IP** pour la communication entre le client et le serveur, avec un serveur capable de gérer plusieurs connexions simultanées.

## 🔧 Technologies utilisées

- **Java** : Langage choisi pour sa simplicité et ses fonctionnalités de haut niveau.
- **TCP/IP** : Protocole de communication pour la gestion des connexions.
- **UDP** : Protocole pour des échanges plus simples entre le client et le serveur.

## ⚙️ Fonctionnalités principales

### **Gestion des utilisateurs :**
- Le serveur peut gérer jusqu'à **4 utilisateurs** 👥.
- Chaque utilisateur est identifié par un **nom d'utilisateur** et un **mot de passe** 🔑.

### **Messagerie :**
- Les utilisateurs peuvent échanger des messages en **temps réel** ou en **mode boîte à lettres** 📨.
- Les messages sont structurés sous la forme : `"login,commande,param1,param2,..."`.

### **Limite d'amis :**
- Chaque utilisateur peut avoir jusqu'à **4 amis** 👯‍♂️.

### **Consultation des messages :**
- Un utilisateur peut consulter ses **10 derniers messages reçus** 📬.

### **Invitations d'amis :**
- Un utilisateur peut envoyer une **invitation d'ami** avec la commande `"demande_ami,login,ami"` 👋.

### **Répliques automatiques :**
- Le serveur réplique automatiquement à tous les amis de l'émetteur lorsqu'un message est envoyé à `"TOUS"` 📢.

### **Notifications :**
- Lorsqu'une invitation est acceptée, l'utilisateur invitant reçoit une **notification** 🎉.

## 🖥️ Fonctionnement du serveur

- Le serveur écoute sur le **port UDP 3333** pour recevoir les messages des clients.
- Les données sont stockées en **RAM** 💾.
- Les commandes principales sont :
  - Envoi de message : `"message,login,ami,sujet,corps"`
  - Invitation à devenir ami : `"demande_ami,login,ami"`
  - Lecture de messages : `"lecture,login"`

## 🛑 Limitations

- Le serveur peut gérer jusqu'à **4 utilisateurs**.
- Le serveur conserve uniquement les **10 derniers messages reçus**.
