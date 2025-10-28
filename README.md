# Nshile
Nshìlé: Peut se traduire par «le regard du peuple» en langue Baham, pour souligner l'attention portée à la population.

Le projet vise à mettre en place un systeme d'analyse de la popularité des personnalités publique en se basant sur du contenu facebook.

De base dans le concept d'analyse de sentiment, le corpus analysé peut être vu sous divers angles:

- La tonalité:
tonalite = [
"Comique : Vise à faire rire le lecteur."
"Dramatique : Utilise un ton intense et souvent violent, avec des thèmes de mort, de souffrance, ou de drame."
"Didactique : Cherche à enseigner ou à instruire le lecteur."
"Épique : Raconte des exploits héroïques, souvent guerriers, de manière spectaculaire."
"Fantastique : Introduit un élément surnaturel et angoissant dans le réel."
"Humoristique : Propose une vision légère et drôle des choses."
"Ironique : Dit le contraire de ce que l'on pense pour critiquer de manière subtile."
"Lyrique : Exprime les sentiments personnels de l'émetteur, souvent avec émotion."
"Pathétique : Cherche à émouvoir le lecteur en accentuant la misère et la souffrance."
"Polémique : Provoque la confrontation d'idées pour débattre ou critiquer de manière passionnée."
"Poétique : Utilise un langage esthétique et recherché pour évoquer des émotions."
"Satirique : Critiquer en se moquant, souvent pour dénoncer des travers."
"Tragique : Met en scène des personnages confrontés à un destin funeste, suscitant la pitié et la terreur." ]

- La polarité:
polarite = [
    "Positif : Exprime une opinion favorable"
    "Négatif : Exprime une opinion défavorable"
    "Neutre : Indique une absence d'opinion ou une description factuelle"
]
polarite_fine = [
    "Très positif", "Positif", "Neutre", "Négatif", "Très négatif"
]

- L'émotion:
emotions = [
    "Amour", "Joie", "Colère", "Tristesse", "Peur", "Surprise", "Dégoût"

]

Ce projet est divisé en deux steps principaux: 

-> LE BACKEND PYTHON

Basé sur une application Web streamLit, le backend doit permettre de set les mots clés (nom de personnalité à analyser), set la liste des pages facebook a scrapper

un script APPIFY nous permettra de scrapper les données sur chacune des pages qui ont été set plus haut.

une fois les données optenue et nettoyée, elle doivent ensuite être analysée par une modèle IA qui pour chaque phrase, va préciser la polarité, l'emotion et la tonalité de la phrase puis préciser le seujet (personnalité concerné par la phrase).

Une fois ces données analysée par le modèle, les données seront stockée dans un entrepot de données sour SQL Server grace a des Job Talend pour être consommés par le dashboard par la suite


-> LE DASHBOARD POWERBI
