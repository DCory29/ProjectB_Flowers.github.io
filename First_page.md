---
layout: default
title: "🧪 The Legend of Giulia Tofana 🧪"
---
<link rel="stylesheet" href="{{ '/assets/css/style.css' | relative_url }}">
<table width="100%">
  <tr>
    <td valign="top" width="50%">
      <img src="img/GiuliaTofana.png" alt="Giulia Tofana" width="90%">
    </td>
    <td valign="top" width="40%">
      <h3> A powerful figure</h3>
      <p>Giulia Tofana who was born around the year 1620 and who died in 1651 in Italy is a fascinating figure of the 17th-century. She is remembered for orchestrating one of the most prolific poisoning networks in early modern Europe. In an era where women did not have many legal rights and thus were often trapped in abusive marriages. She provided a lethal escape route for hundreds of desperate wives.</p>
    </td>
  </tr>
</table>



### 🏛️ Myth vs. Historical Reality 🏛️
While pop culture and history often blur, modern research highlights key distinctions between the myth and the historical record:

*The Popular Legend*

According to the popular legend, she confessed to killing 600 men under brutal torture then got arrested, tortured, and publicly executed in Rome’s Campo de’ Fiori in 1659 
She is viewed strictly as one of history’s most prolific serial killers.



*The Historical Reality*

In fact, she died peacefully in her sleep in 1651, never having been convicted.
The famous 1659 trial actually prosecuted Gironima Spana and her network, who had inherited the formula.
It was seen by historians as a tragic, criminal response to a *suffocating patriarchal society*.

### 💧The Perfect Weapon💧
<table width="100%">
  <tr>
    <td valign="top" width="40%">
      <p>Giulia formulated a deadly poison known as **Aqua Tofana**. Its unique properties made it the ultimate tool for the perfect crime:
She used a lethal mixture of arsenic, lead, and belladonna. Those ingredients were completely colorless, odorless, and tasteless, making it easy to blend into water or wine.
Administered a few drops at a time over several days, it mimicked a slow, natural illness, leaving 17th-century doctors clueless*e.
**The Disguise:** The poison was sold disguised as a cosmetic face cream or in devotional vials labeled "Manna of St. Nicholas of Bari" to evade the authorities.</p>
    </td>
    <td valign="top" width="60%">
      <img src="img/AquaTofana.png" alt="Aqua Tofana" width="100%">
    </td>
  </tr>
</table>

### The Network and Impact
<table width="100%">
  <tr>
    <td valign="top" width="40%">
      <p>Giulia formulated a deadly poison known as **Aqua Tofana**. Its unique properties made it the ultimate tool for the perfect crime:
Operating first in Palermo and later in Rome, Giulia did not work alone. She surrounded herself with a trusted inner circle of women, including her stepdaughter (or close associate) **Gironima Spana**. 

Rumor has it they built a secretive word-of-mouth network. Historical estimates (largely derived from later trials) attribute the deaths of **over 600 men**—mostly abusive husbands—to her poison between 1633 and 1651.
</p>
    </td>
    <td valign="top" width="60%">
      <img src="img/GiuliaAccomplice.png" alt="Giulia Accomplice" width="100%">
    </td>
  </tr>
</table>

## 🌟 Legacy 🌟
<p align="center">
  <img src="img/Legend.png" alt="Legend" width="100%">
</p>
The impact of Aqua Tofana echoed through the centuries. It heavily influenced France's infamous "Affair of the Poisons" during the reign of Louis XIV. Decades later, while on his deathbed in 1791, the legendary composer Wolfgang Amadeus Mozart famously claimed he was being poisoned with Aqua Tofana.


***
*Sources & Further Reading: [National Geographic](https://nationalgeographic.com) & [Wikipedia](https://wikipedia.org)*

***
[Sally Basset's story](Second_page) --- [Baba Anujka's story](Third_page)
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
