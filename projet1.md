Le jeu est composé de trois scènes principales :

## 1. Menu principal
- Affichage du titre Emoji Match  
- Bouton “Start Level 1”  
- Effet sonore lors du clic  
- Passage direct à la scène de jeu du niveau 1  

## 2. Jeu principal
### Objectif  
Trouver toutes les paires avant la fin du temps.

### Caractéristiques du niveau  
- Niveau 1 : 8 paires, 60 secondes  
- Niveau 2 : 12 paires, 90 secondes  

### Logique du jeu  
- Les cartes sont affichées sous forme d’émojis cachés (“❓”).  
- Le joueur clique pour révéler une carte.  
- Deux cartes révélées = comparaison :  
  - Même emoji : paire trouvée  
  - Emoji différent : cartes retournées après 0,8 seconde  

### Interface affichée  
- Compteur de temps (Time)  
- Score (Found)  
- Icône pour activer ou mettre en pause la musique d’ambiance  

### Fin du niveau  
- Temps écoulé : affichage “Time Over” et bouton Restart  

## 3. Transition de niveau (LevelTransition)
Lorsqu’un joueur termine le niveau 1 :

- Message “Félicitations !”  
- Bouton “Level 2”  
- Son de clic  

# Gestion du son
Le jeu intègre :

- un son de clic  
- un son lors d'une mauvaise paire  
- une musique d’ambiance en b
