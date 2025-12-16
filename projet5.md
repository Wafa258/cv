# ✅ Améliorations apportées : 

### 1️. Ajout de 4 thèmes 

Le joueur choisit son thème (Emoji, Animaux, Fruits & Légumes, Sports) avant de démarrer le niveau.

Les boutons de thème changent de couleur lorsqu’ils sont sélectionnés.

J'ai rajouté ces lignes dans le code : 

const THEMES = {

  emoji: ['😀','😎','😍','😂','🥰','😜','🤩','😇','😱','🤪','🤓','🤑','🥳','😏','🤠','🤖'],
  
  animals: ['🐶','🐱','🦁','🐯','🐭','🐹','🐰','🐻','🐼','🐨','🐸','🐵','🐔','🦊','🐴','🦄'],
  
  fruits: ['🍎','🍌','🍇','🍉','🍓','🍒','🍑','🍍','🥝','🥥','🍐','🍊','🥕','🍅','🥦','🌽'],
  
  sport: ['⚽','🏀','🏈','⚾','🎾','🏓','🏒','🥊','🎱','🤿','🥋','⛷️','🏄','🚴','⛳','🥅']
  
};

  et j'ai demandé à ChatGPT de me créer un tableau pour stocker les boutons de thème
  
    this.themeButtons = [];

  Je lui ai également demandé de rajouter une fonction pour gérer la sélection du thème
  
    const selectTheme = (themeName, btn) => {
    
      selectedTheme = themeName;
      
      this.sound.play('click');
      
  Et de ettre en surbrillance le bouton sélectionné
    
      btn.getAt(0).setFillStyle(0xFF99CC);
