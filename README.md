# Tableau de Bord Power BI – Analyse des Ventes
  
Technologies : Power BI, DAX, Excel  
Projet : Tableau de bord interactif pour l’analyse des ventes, des clients et des régions


## 📌 Objectif du projet
Ce projet a pour but de créer un dashboard interactif permettant de :

- Suivre le Chiffre d’Affaires, le Bénéfice et la Marge  
- Identifier les Top Produits  
- Visualiser la répartition géographique des ventes par région


## 📊 KPIs principaux
1. Chiffre d’Affaires Total  
2. Bénéfice Total  
3. Marge (%)


## ❓ Questions d’analyse traitées
- Quels sont les Top 10 Produits les plus rentables ?  
- Quels sont les Top 10 Clients par chiffre d’affaires ?  
- Quelle région génère le plus de ventes et de bénéfices ?


## 🛠️ Méthodologie
1. Préparation des données : Excel → Power BI  
2. Création du modèle relationnel :  
   - `Ventes → Produits`  
   - `Ventes → Clients`  
   - `Ventes → Régions`  
3. Mesures DAX calculées :  
   ```DAX
   ChiffreAffaires = SUMX(Ventes, Ventes[Quantité]*Ventes[Prix_Unitaire])
   Bénéfice = SUMX(Ventes, (Ventes[Prix_Unitaire]-Ventes[Coût_Unitaire])*Ventes[Quantité])
   Marge = DIVIDE([Bénéfice],[ChiffreAffaires])
   NombreClients = DISTINCTCOUNT(Ventes[ClientID])

##🚀 Comment utiliser ce projet

1.Télécharge les fichiers .pbix et .xlsx

2.Ouvre le fichier .pbix dans Power BI Desktop

3.Vérifie que les tables sont correctement liées

4.Explore le dashboard et teste les filtres interactifs