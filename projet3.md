# ✅ Améliorations apportées : 

### 1. Timer amélioré

Emoji ⏳ ajouté dès le départ devant le texte du timer.

Changement de couleur en rouge et clignotement du timer lorsqu'il est inférieur à 10 secondes. Cela créé un effet de pression. 

Le timer reste normal (noir, pas de clignotement) tant qu’il reste plus de 10 secondes.

J'ai demandé à ChatGPT de me fournir le code que j'ai du ajuster par la suite :

 // Timer avec clignotement rapide et rouge quand <10s
 
    this.clignotementTween = null;
    
    this.timerEvent = this.time.addEvent({
    
      delay: 1000,
      
      loop: true,
      
      callback: () => {
      
        this.timeLeft--;
        
        this.timerText.setText('⏳ Time: ' + this.timeLeft);
        

        if (this.timeLeft === 10) {
        
          // rouge + clignotement rapide
          
          this.timerText.setColor('#FF0000');
          
          this.clignotementTween = this.tweens.add({
          
            targets: this.timerText,
            
            alpha: 0,
            
            duration: 250,
            
            yoyo: true,
            
            repeat: -1
            
          });
          
        }

### 2️. Boutons améliorés (hover)

Les boutons suivants ont été améliorés :
“Start Level 1” dans le menu principal.
“Level X” dans l’écran de transition entre niveaux.
“Restart” à la fin du jeu.

Effets au hover :
Scale / agrandissement léger au survol.
Glow / contour jaune autour du bouton pour attirer l’œil.
L’effet est réversible : quand la souris quitte le bouton, il redevient normal.
L’animation est fluide et répétitive (pulsation légère).
