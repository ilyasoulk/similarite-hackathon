# Journal de Bord (Cheallenge 6milarité)

- Team 5



# Jour 1


### 1. Mise en place des environnements de collaboration

- GitHub : Nous avons mis en place un dépôt Git pour versionner et partager notre code. Cela nous permet également de collaborer pour fludifier l'effort collectif.

- Slack : Pour nous permettre d'échanger entre nous et de suivre les différentes consignes du challenge.

<br>


A partir de là, l'équipe s'est séparée afin de pouvoir traiter en parallèle les tâches de `Data Engineering`, d'`Analyse Exploratoire` et de `Modeling (Transfer Learning)`.


## 2. Data Engineering


- **Téléchargement des données avec API Kagle de Python**: Au début du challenge, nous nous sommes rendu compte que la grosse volumétrie de nos données causait un long téléchargment. Nous avons donc cherché une solution plus rapide et nous avons découvert une API Kaggle compatible avec Python qui nous nous a permis de télécharger nos données plus rapidement.


- **Groupement des données**: Pour pouvoir obtenir les noms de modèles pour chaque donnée du train et du test set, nous avons effectué des jointures entre nos données. Ces tables jointes seront utilisées ensuite dans notre `Analyse Exploratoire`.


- **Feature Engineering**: Pour une analyse et une réflexion plus poussée et complète, nous avons crée de nouvelles variables. Ainsi, nous avons extrait l'`année` de chaque classe, le `nom du modèle sans l'année`, ainsi que la `marque`de la voiture. Nous décrirons ensuite nos données en analysant en plus ces nouvelles données.


## 3. Analyse Exploratoire des Données (EDA)

Cette partie nous a permis de mieux comprendre les données mises à notre disposition.

- **Distribution des classes**: La distribution des classes dans le test set est similaire à celle du training set. Cela signifie que le modèle sera évalué sur un ensemble de données représentatif des données réelles d'entrainement.

![classes_distribution](img/class_dist.png)


- **Distribution des classes dans l'ensemble des données**: On observe une distribution déséquilibrée, avec certaines classes plus fréquentes que d'autres. Le modèle pourrait être biaisé en faveur des classes majoritaires, ce qui signifie qu'il pourrait être plus performant pour reconnaître ces classes et moins performant pour reconnaître les classes minoritaires.

![class_barplot](img/class_barplot.png)

![class_barplot](img/year_barplot.png)

![class_barplot](img/model_name_barplot.png)

![class_barplot](img/marque_barplot.png)



| Category | Top 5 | Tail 5 |
|:-----------|:-----------|:-----------|
|**Classes de voiture** | - Chevrolet Corvette ZR1 2012<br>- Mitsubishi Lancer Sedan 2012<br>- Mercedes-Benz 300-Class Convertible 1993<br>- Chrysler 300 SRT-8 2010<br>- GMC Savana Van 2012 | - Hyundai Accent Sedan 2012<br>- FIAT 500 Abarth 2012<br>- Maybach Landaulet Convertible 2012<br>- Chevrolet Express Cargo Van 2007<br>- Rolls-Royce Phantom Drophead Coupe Convertible 2012 | 
|**Modèle sans les années** | - Honda Odyssey Minivan <br>- Audi S4 Sedan <br>- Ford F-150 Regular Cab <br>- Volkswagen Golf Hatchback <br>- Dodge Durango SUV  | - Hyundai Accent Sedan<br>- FIAT 500 Abarth<br> - Maybach Landaulet Convertible<br>- Chevrolet Express Cargo Van<br>- Rolls-Royce Phantom Drophead Coupe Convertible | 
|**Marques des voiture** | - Ford<br>- BMW<br>- Audi<br>- Dodge<br>- Chevrolet | - Maybach<br>- Mazda<br>- MINI<br>- Tesla<br>- Lincoln | 



## 4. Modelling (Transfer Learning)

Cette partie a servi surtout à mieux comprendre et tester les performances de notre modèle.

Il est important d'avoir un ensemble de données d'entraînement équilibré, pour compenser ce déséquilibre nous avons opté pour : 

- Échantillonnage aléatoire: nous avons d'abord groupé le train et le test set puis `... `(sous-échantillonner les classes majoritaires et suréchantillonner les classes minoritaires. 


- Pondération des classes: cela consisterait à pondérer les classes pendant l'entraînement. Chaque classe minoritaire reçoit un poids plus important pendant l'entraînement, ce qui permet au modèle de mieux apprendre les caractéristiques de ces classes. Toutefois, nous n'avons pas implémenté cette méthode.



# Jour 2


# Jour 3
