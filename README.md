# CoopQuote AI - Assistant de Chiffrage B2B 

**CoopQuote AI** est un PoC (Proof of Concept) d'assistant commercial intelligent conçu pour automatiser et sécuriser la génération de devis B2B pour les coopératives (ex: Unipros).

---

##  Problématique & Inconvénients Métier
* **Perte de temps :** 2 à 3 heures par proposition commerciale rédigée à la main.
* **Risque d'erreur :** Oubli des remises coopératives sur volume et mauvais calculs de TVA.
* **Complexité :** Difficulté à garantir la conformité avec la politique tarifaire globale.

---

##  Architecture Technique & Choix Produit

1. **System Prompting Métier :**
   * Encadrement strict du LLM pour éliminer les hallucinations.
   * **Règle RM-01 :** Application automatique du taux de TVA B2B à 20%.
   * **Règle RM-02 :** Remise coopérative automatique de 15% pour toute commande > 10 unités.
   * Restitution des réponses au format **JSON structuré**.

2. **Interface Utilisateur (UI) :**
   * Interface légère et réactive développée en HTML5 & Tailwind CSS.
   * Gestion des états de chargement (*UI Loading States*) pour une meilleure expérience utilisateur.

3. **Sécurité & Variables d'Environnement :**
   * Isolation des clés API sensibles dans des fichiers `.env` ignorés par Git via `.gitignore`.

4. **Souveraineté des Données & IA Locale (Ollama) :**
   * Expérimentation et déploiement du modèle **Llama 3** en local via **Ollama**.
   * Traitement hors-ligne garantissant la confidentialité des données tarifaires sensibles et le respect du RGPD.

5. **Intégration Workflows & Automatisations (Webhooks) :**
   * Architecture pensée pour s'intégrer aux flux existants (CRM / WordPress).
   * Déclenchement automatique par **Webhooks** pour mettre à jour les fiches clients et générer les devis sans intervention humaine.

---

## Lancer le projet en local

1. Cloner le dépôt :
   ```bash
   git clone [https://github.com/Chrystelle974/coopquote-ai.git](https://github.com/Chrystelle974/coopquote-ai.git)