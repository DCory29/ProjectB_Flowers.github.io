---
layout: default
title: Accueil
---

# Project Poisonous Flowers
<p align="center">
   <img src="./img/Poisonous.png" width="820" height="542">
</p>
 
  > *For centuries, women have been compared to flowers.*
> *Little did they know they were not so wrong to make such an accurate comparison. Much like the most captivating flora in nature, women possess a breathtaking beauty—but when threatened, some carry a lethal defense. On this site, you'll find three stories of three women who turned the traditional symbol of femininity into a weapon of survival, rebellion, and ultimate power.*



---

### 🌿 Table of contents 🌿


*   *[🧪The Legend of Giulia Tofana🧪](./First_page)*
*   *[🪻The Legend of Sally Bassett🪻](Second_page)*
*   *[🥀The Story of Baba Anujka🥀](Third_page)*


> [!WARNING] > **Disclaimer:** Please be aware that the following content are either historical facts or legends; I do not condone or encourage any of these methods. Additionally, sensitive topics such as domestic violence and poisoning are discussed, which might be distressing to some readers.

---

<div id="leaf-container" style="position: fixed; top: 0; left: 0; width: 100%; height: 100%; overflow: hidden; pointer-events: none; z-index: 9999;"></div>


<button id="theme-toggle">🌙 Mode Sombre</button>

<script>
  
  (function() {
    if (localStorage.getItem('theme') === 'dark') {
      document.documentElement.classList.add('dark-mode');
    }
  })();

  document.addEventListener('DOMContentLoaded', () => {
    const toggleBtn = document.getElementById('theme-toggle');
    const htmlEl = document.documentElement;
    const bodyEl = document.body;

    // Synchronisation du bouton et de l'état
    if (htmlEl.classList.contains('dark-mode')) {
      bodyEl.classList.add('dark-mode');
      if (toggleBtn) toggleBtn.textContent = '☀️ Mode Clair';
    }

    if (toggleBtn) {
      toggleBtn.addEventListener('click', () => {
        htmlEl.classList.toggle('dark-mode');
        bodyEl.classList.toggle('dark-mode');
        if (htmlEl.classList.contains('dark-mode')) {
          toggleBtn.textContent = '☀️ Mode Clair';
          localStorage.setItem('theme', 'dark');
        } else {
          toggleBtn.textContent = '🌙 Mode Sombre';
          localStorage.setItem('theme', 'light');
        }
      });
    }

    
    const container = document.getElementById('leaf-container');
    const leaves = ['🍁', '🍂', '🍃', '🌱']; 

    if (container) {
      function createLeaf() {
        const leaf = document.createElement('div');
        leaf.classList.add('leaf');
        leaf.innerText = leaves[Math.floor(Math.random() * leaves.length)];
        leaf.style.left = Math.random() * 100 + 'vw';
        const duration = Math.random() * 5 + 5;
        leaf.style.animationDuration = duration + 's';
        leaf.style.fontSize = Math.random() * 10 + 14 + 'px';
        leaf.style.opacity = Math.random() * 0.6 + 0.3;
        container.appendChild(leaf);
        setTimeout(() => { leaf.remove(); }, duration * 1000);
      }
      setInterval(createLeaf, 450);
    }
  });
</script>
      setInterval(createLeaf, 450);
    }
  });
</script>
