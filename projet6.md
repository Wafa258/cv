# ✅ Améliorations apportées :

### 1. Ajout du mode nuit 
Ajout de l'icone lune 🌙 en haut à droite pour choisir le mode nuit / normal.

Les textes et les cartes passent en couleurs néon pour bien contraster avec le fond.
Cela permet de jouer confortablement dans une ambiance plus sombre.

J'ai rajouté ce code pour cette fonctionnalité : 

 updateNightMode(){
 
    if(nightMode){
    
      this.background.setFillStyle(0x0D1B2A);
      
      this.cards.forEach(c => c.setColor('#0ff'));
      
      this.timerText.setColor('#0ff');
      
      this.scoreText.setColor('#0ff');
      
    } else {
    
      let bgColor;
      
      switch(this.theme){
      
          case 'emoji': bgColor = 0xDDB8F2; break;
          
          case 'animals': bgColor = 0xA8E6CF; break;
          
          case 'fruits': bgColor = 0xFFD3B6; break;
          
          case 'sport': bgColor = 0xFFAAA5; break;
          
      }
      this.background.setFillStyle(bgColor);
      
      this.cards.forEach(c => c.setColor('#000'));
      
      this.timerText.setColor('#333');
      
      this.scoreText.setColor('#333');
      
    }
    
  }
  

  Et je l'ai appelé au début du code : 
  let nightMode = false;


### 2. Changer la couleur de fond selon le thème

Chaque thème a sa propre couleur de fond dans la scène de jeu :
Emoji → violet clair
Animaux → vert clair
Fruits → orange clair
Sport → rose clair

J'ai demandé à ChatGPT de me séléctionner le thème choisit : 

      createButton(this,450,450,'Start Level 1','#FFFFFF',0xF2509B,()=>{ 
   
      this.scene.start('MainGame',{level:1, theme:selectedTheme}); 

### 3. Animation plus fluide pour les cartes

Lorsqu’une carte est révélée, elle “tourne” horizontalement avant d’afficher son emoji.
Les cartes non assorties retournent aussi avec un petit effet de rotation.
Cela rend le jeu plus dynamique et agréable visuellement.
