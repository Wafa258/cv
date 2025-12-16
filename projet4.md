# ✅ Améliorations apportées : 

### 1. Ajout d'un 3ème niveau plus difficile
time: 120 secondes, paires: 15

J'ai rajouté cette ligne dans script pour le niveau 3 en m'appuyant sur le code des autres niveaux : 

const levels = [
  
  
  { time: 120, pairs: 15 }
];
  

### 2. Animation spécifique pour les bonnes paires 
  
Pop / tween scale quand deux cartes matchent, pour donner une sensation de récompense.

### 3. Ajout de l'icône pause, 
On peut arrêter le jeu, et reprendre plus tard, le timer s'arrête. 

J'ai demandé à ChatGPT de me fournir le code pour mettre en pause le jeu, il m'a fournit ce code :

  this.pauseText = this.add.text(50,bottomY,'⏸️',{fontSize:'40px',color:'#F2509B'}).setOrigin(0.5).setInteractive();
  
    this.pauseText.on('pointerdown',()=>{ 
    
      this.scene.pause();
      
      this.scene.launch('PauseScene',{parent:this}); 
      
    });
    
    this.pauseText.on('pointerover',()=>this.pauseText.setColor('#FF85C1'));
    
    this.pauseText.on('pointerout',()=>this.pauseText.setColor('#F2509B'));
    

### 4. Boutons modernisés : Start Level, Level X, Restart, Resume
Cadre coloré, texte centré, hover léger avec mise à l’échelle.
