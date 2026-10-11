---
layout: default
title: Accueil
---
<link rel="stylesheet" href="{{ '/assets/css/style.css' | relative_url }}">

# Project Poisonous Flowers
<p align="center">
   <img src="./img/Poisonous.png" width="320" height="342">
</p>
 
  > *For centuries, women have been compared to flowers.*
> *Little did they know they were not so wrong to make such an accurate comparison*






---

### 🌿 Table of contents 🌿


*   *[🧪 The Legend of Giulia Tofana](./First_page)*
  
*   *[🪻 The Legend of Sally Bassett🪻](Second_page)*
*   *[🥀The Story of Baba Anujka🥀_](Third_page)*


> [!WARNING] > **Disclaimer:** Please be aware that the following content are either historical facts or legends; I do not condone or encourage any of these methods. Additionally, sensitive topics such as domestic violence and poisoning are discussed, which might be distressing to some readers.

---

<button id="theme-toggle">🌙 Mode Sombre</button>

<script>
  const toggleBtn = document.getElementById('theme-toggle');
  const body = document.body;

  if (localStorage.getItem('theme') === 'dark') {
    body.classList.add('dark-mode');
    toggleBtn.textContent = '☀️ Mode Clair';
  }

  toggleBtn.addEventListener('click', () => {
    body.classList.toggle('dark-mode');
    if (body.classList.contains('dark-mode')) {
      toggleBtn.textContent = '☀️ Mode Clair';
      localStorage.setItem('theme', 'dark');
    } else {
      toggleBtn.textContent = '🌙 Mode Sombre';
      localStorage.setItem('theme', 'light');
    }
  });
</script>
