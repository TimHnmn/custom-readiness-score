# 🏃‍♂️ Custom Readiness Score Algorithm

**Algorithme personnalisé de score de récupération physique basé sur l'analyse de données biométriques Oura Ring.**

---

## 🎯 Objectif

Développer un algorithme de récupération personnalisé en analysant 5 mois de données physiologiques (septembre 2025 - janvier 2026). L'objectif est d'identifier les facteurs clés de récupération et de créer un score plus adapté à mon profil que l'algorithme standard d'Oura.

---

## 📊 Données

- **Source :** Oura Ring (export Cloud)
- **Période :** Septembre 2025 - Janvier 2026 (~150 jours)
- **Métriques :**
  - HRV (Heart Rate Variability)
  - RHR (Resting Heart Rate)
  - Sommeil (Total, Deep, REM, Light, Efficiency)
  - Temperature Deviation
  - Readiness Score (cible)
  - Sleep Score

---

## 🛠️ Stack Technique

- **Python 3.11**
- **Pandas** - Manipulation de données
- **NumPy** - Calculs numériques
- **Matplotlib / Seaborn** - Visualisations
- **Scikit-learn** - Machine Learning

---

## 📁 Structure du Projet
```
custom-readiness-score/
├── data/                  # Données brutes
├── notebooks/             # Notebooks d'exploration
├── src/                   # Code Python réutilisable
├── results/               # Graphiques et résultats
├── README.md
├── requirements.txt
└── .gitignore
```

---

## 🚀 Installation
```bash
# Cloner le projet
git clone https://github.com/ton-username/custom-readiness-score.git
cd custom-readiness-score

# Créer l'environnement virtuel
conda create -n readiness python=3.11 -y
conda activate readiness

# Installer les dépendances
pip install -r requirements.txt
```

---

## 📈 Résultats Clés

*(À compléter après l'analyse)*

- **Facteur #1 :** HRV (XX% de corrélation avec Readiness)
- **Facteur #2 :** RHR (XX% de corrélation)
- **Facteur #3 :** Sommeil (XX% de corrélation)

**Précision du modèle :** R² = X.XX

---

## 📊 Visualisations

*(Screenshots à ajouter)*

---

## 👤 Auteur

**Ton Nom**  
[LinkedIn](lien) | [GitHub](lien)

---

## 📝 License

Ce projet est à usage personnel et éducatif.