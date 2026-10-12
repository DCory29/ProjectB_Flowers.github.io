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

<!-- CONTENEUR DES FEUILLES QUI TOMBENT -->
<div id="leaf-container" style="position: fixed; top: 0; left: 0; width: 100%; height: 100%; overflow: hidden; pointer-events: none; z-index: 9999;"></div>

<!-- BOUTON DU MODE SOMBRE PARFAITEMENT ALIGNÉ -->
<div style="text-align: right; padding: 10px 0;">
  <button id="theme-toggle" style="padding: 5px 12px; cursor: pointer; border-radius: 4px; border: 1px solid #ccc; background: transparent; color: inherit; font-size: 0.9rem;">🌙 Mode Sombre</button>
</div>

<!-- LE STYLE ET LE SCRIPT LOGIQUE SANS CONFLIT -->
<style>
  html.dark-mode body, html.dark-mode { background-color: #1a1a1a !important; color: #f5f5f5 !important; }
  .leaf { position: absolute; top: -50px; font-size: 24px; user-select: none; pointer-events: none; animation: fall linear infinite; }
  @keyframes fall {
    0% { transform: translateY(0) rotate(0deg) translateX(0); opacity: 1; }
    100% { transform: translateY(105vh) rotate(360deg) translateX(50px); opacity: 0.3; }
  }
</style>

<script>
  // 1. SCRIPT ANTI-FLASH IMMEDIATE
  if (localStorage.getItem('theme') === 'dark') {
    document.documentElement.classList.add('dark-mode');
  }

  // 2. EXÉCUTION UNE FOIS LA PAGE COULÉE DANS LE THÈME
  document.addEventListener('DOMContentLoaded', () => {
    const toggleBtn = document.getElementById('theme-toggle');
    const htmlEl = document.documentElement;
    const bodyEl = document.body;

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

    // GÉNÉRATEUR DE FEUILLES EN CASCADE
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
