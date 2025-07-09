# 🧬 etiennevar

**etiennevar** est un outil en ligne de commande (CLI) léger et performant développé pour explorer, résumer et visualiser les fichiers VCF (`.vcf` et `.vcf.gz`), couramment utilisés en génétique pour décrire des variants. Il est destiné aussi bien aux bioinformaticiens débutants qu’aux utilisateurs avancés travaillant avec des jeux de données génomiques.

---

## 🚀 Installation

### Depuis PyPI

```bash
pip install etiennevar
```

### Ou localement depuis GitHub

```bash
git clone https://github.com/EtienneNtumba/etiennevar.git
cd etiennevar
pip install .
```

---

## 🎯 Objectif de l’outil

L’analyse des fichiers VCF est une étape critique dans les études de génétique et de génomique. Pourtant, il n’est pas toujours trivial d’obtenir un résumé rapide ou une visualisation simple des variants présents. **etiennevar** répond à ce besoin par une interface intuitive permettant :

- De résumer le contenu d’un fichier VCF (nombre de variants, chromosomes présents)
- De filtrer les variants par chromosome ou par intervalle génomique
- De visualiser la distribution des variants sous plusieurs formats de graphique (histogramme, boxplot, violon, circle plot)
- D’obtenir des statistiques sommaires : moyenne, médiane, nombre total, etc.

---

## 📦 Fonctionnalités

| Option           | Description |
|------------------|-------------|
| `--summary`       | Affiche un résumé des variants dans le fichier VCF |
| `--plot`          | Génère une visualisation de la distribution des variants |
| `--plot-type`     | Type de graphique : `hist`, `box`, `violin`, `circle` (par défaut : `hist`) |
| `--summary-stat`  | Affiche des statistiques descriptives détaillées |
| `--chr`           | Filtre les variants selon un ou plusieurs chromosomes |
| `--range`         | Filtre les variants selon une plage de positions (ex : `--range 1000 5000`) |
| `--output`        | Spécifie le nom du fichier image à générer |
| `--version`       | Affiche la version de l’outil |

---

## 📈 Exemples d’utilisation

### Résumé rapide d’un VCF

```bash
etiennevar --summary data.vcf.gz
```

### Résumé avec filtrage

```bash
etiennevar --summary --chr 1 2 X --range 10000 50000 data.vcf.gz
```

### Génération d’un histogramme

```bash
etiennevar --plot --plot-type hist --output histogram.png data.vcf.gz
```

### Graphique de type violon + stats

```bash
etiennevar --plot --plot-type violin --summary-stat data.vcf.gz
```

---

## 🧪 Exemples de fichiers

Des exemples de fichiers VCF sont disponibles dans le dépôt :

- `converted_snps.vcf`
- `uncompressed.vcf`

Ces fichiers peuvent être utilisés pour tester les fonctionnalités de l’outil.

---

## 🔧 Dépendances

- `matplotlib`
- `numpy`
- `seaborn` *(nécessaire pour les graphes de type boxplot et violon)*

Les dépendances sont automatiquement installées avec :

```bash
pip install etiennevar
```

---

## 👤 Auteur

Développé par **Etienne Kabongo Ntumba**, étudiant-chercheur en bioinformatique et génétique statistique, passionné par l’analyse des données génomiques à grande échelle et la reproductibilité scientifique.

📧 Email : etiennekabongo.bioinfo@gmail.com  
🔗 LinkedIn / GitHub : [@EtienneNtumba](https://github.com/EtienneNtumba)

💡 Contribuez, signalez des bugs ou proposez des améliorations via les [issues GitHub](https://github.com/EtienneNtumba/etiennevar/issues)

---

## 📜 Licence

Ce projet est distribué sous licence MIT. Vous êtes libre de l'utiliser, le modifier et le distribuer avec attribution.
