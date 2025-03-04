🏀 NBA Stats Scraper & Analysis
🔍 Description
Ce projet vise à extraire, analyser et prédire les performances des joueurs NBA à partir des statistiques de la saison 2020-2021. Les données sont issues de Basketball Reference et permettent d'explorer divers aspects du jeu comme les meilleurs marqueurs, la polyvalence des joueurs, l'efficacité offensive des équipes et la prédiction des points par match.

Données scrapées
📌 Source : Basketball Reference - Saison NBA 2020-2021

📊 Colonnes extraites :

Colonne	Description
Rk	Rank (Classement)
Player	Nom du joueur
Age	Âge du joueur au 1er février de la saison
Team	Équipe
Pos	Position du joueur
G	Nombre de matchs joués
GS	Nombre de matchs commencés en tant que titulaire
MP	Minutes jouées
PTS	Points marqués
AST	Assists (Passes décisives)
TRB	Total Rebounds (Total de rebonds)
STL	Steals (Interceptions)
BLK	Blocks (Contres)
FG%	Pourcentage de réussite aux tirs
3P%	Pourcentage de réussite aux tirs à 3 points
FT%	Pourcentage de réussite aux lancers francs
TOV	Turnovers (Ballons perdus)
PF	Personal Fouls (Fautes personnelles)
Awards	Récompenses reçues
❓ Questions étudiées
Question principale	Sous-questions	Analyses effectuées
Qualité des données ?	1. Présence de NaNs, types de données ? 2. Catégories et distribution des variables ?	- pandas.info(), .describe() - Histogrammes et boxplots (seaborn.histplot(), seaborn.boxplot())
Qui sont les meilleurs marqueurs ?	1. Top 10 des marqueurs par game. 2. Distribution des points par match.	- seaborn.barplot() pour le top 10 - seaborn.histplot() pour la distribution des points
Qui sont les joueurs les plus polyvalents ?	1. Joueurs équilibrés. 2. Corrélation points/rebonds/passes.	- seaborn.scatterplot() (différenciation des joueurs) - seaborn.heatmap() (corrélations PTS/TRB/AST)
Quelles sont les équipes les plus offensives ?	1. Top 5 des équipes offensives. 2. Distribution des points par équipe.	- seaborn.barplot() (points moyens par équipe) - seaborn.boxplot() et seaborn.violinplot()
Qui a le meilleur ratio points/minutes ?	1. Top 10 des joueurs efficaces. 2. Corrélation minutes/points.	- seaborn.regplot() (MP vs. PTS avec régression) - seaborn.barplot() (top 10 joueurs efficaces)
Qui sont les joueurs sous-utilisés ?	1. Joueurs performants avec peu de minutes. 2. Répartition par équipe.	- seaborn.barplot() (joueurs sous-utilisés) - seaborn.heatmap() (répartition par équipe)
Prédiction des points par match	1. Variables importantes. 2. Modèle le plus performant.	- seaborn.barplot() (feature importance) - seaborn.scatterplot() (prédictions vs valeurs réelles) - matplotlib (courbes d'erreur)
📊 Résultats de la prédiction
Nous avons utilisé un modèle Random Forest pour prédire les points par match (PTS).

📈 Performance du modèle :

MSE (Mean Squared Error) : 0.384
RMSE (Root Mean Squared Error) : 0.814
R² Score : 0.990
📊 Comparaison des valeurs réelles vs. prédictions :

Joueur (ID)	PTS Réel	PTS Prédiction
478	5.1	5.59
81	16.6	16.41
77	13.0	12.29
208	10.5	10.42
319	7.6	7.31
➡ Les prédictions sont très proches des valeurs réelles, indiquant une bonne précision du modèle.

🔧 Technologies utilisées
🔹 Scraping : requests, BeautifulSoup
🔹 Data Science : pandas, numpy, seaborn, matplotlib, scikit-learn
🔹 Machine Learning : Random Forest Regressor

