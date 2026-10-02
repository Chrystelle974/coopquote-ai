 
# 🚀 CoopQuote AI — Assistant de Chiffrage B2B pour Coopératives

> **Positionnement :** Un outil de génération et d'optimisation de devis commerciaux propulsé par l'IA, conçu pour les indépendants et coopératives B2B.

---

## 🎯 1. Problématique & Proposition de Valeur

* **Problème :** Rédiger des propositions commerciales B2B est une tâche chronophage (2 à 3 heures par devis), sujette aux erreurs de chiffrage et aux omissions d'options.
* **Solution :** Une interface minimale où l'utilisateur décrit le besoin client en une phrase. L'IA structure les lignes de devis, applique les taux de marge coopératifs et génère une proposition prête à l'envoi en **2 minutes**.

---

## 👤 2. Persona Cible
* **Nom :** Alexandre, Artisan / Consultant indépendant en coopérative (ex. Unipros).
* **Besoin :** Gain de temps, zéro erreur de calcul, présentation professionnelle garantie pour ses clients.

---

## 🔄 3. Parcours Utilisateur (User Journey)

1. **Saisie du Besoin (`index.html` / `dashboard.html`)**
   * L'utilisateur saisit une consigne textuelle (ex: *"20 ordinateurs portables pour équipement d'équipe"*).
   * Clic sur **« Générer le devis »**.
2. **Traitement par l'IA**
   * Analyse du besoin, décomposition des lots, calcul des remises de volume coopératives.
3. **Consultation et Édition (`devis-detail.html`)**
   * Affichage du devis structuré : lignes d'articles, sous-totaux, TVA et économies réalisées.
   * Actions possibles : Export PDF, envoi par email ou modification.

---

## 📏 4. Règles Métier (Business Rules)

* **RM-01 (TVA) :** Application automatique du taux standard de 20 % sauf mention d'une prestation exonérée.
* **RM-02 (Marge Coopérative) :** Application d'une remise automatique de 15 % dès lors que la commande dépasse 10 unités.
* **RM-03 (Validation) :** Un devis d'un montant supérieur à 10 000 € HT nécessite un statut *"En attente de validation coopérative"*.

---

## 🛠️ 5. Stack Technique & Architecture PoC

* **Interface UI :** HTML5, Tailwind CSS via CDN (prototypage ultra-rapide).
* **Conception & Prompting :** v0.dev & Claude (génération de composants UI).
* **Version Control :** Git & GitHub (workflow CLI).