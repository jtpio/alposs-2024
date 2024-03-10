---
marp: true
theme: default
paginate: true
footer: ![height:20px](img/twitter.svg) ![height:20px](img/github.svg) @jtpio @QuantStack
style: |
  .columns {
    display: grid;
    grid-template-columns: repeat(2, minmax(0, 1fr));
    gap: 1rem;
  }
---

<style>
section::after {
  content: attr(data-marpit-pagination) '/' attr(data-marpit-pagination-total);
}
img[alt~="center"] {
  display: block;
  margin: 0 auto;
}
</style>

![bg fit right:30%](https://raw.githubusercontent.com/jupyterlite/jupyterlite/main/docs/_static/icon.svg)

# Créer des sites web Jupyter interactifs avec JupyterLite

## AlpOSS 2024

### Jérémy Tuloup

---

# About
<div>

## Jérémy Tuloup

- Directeur Technique à QuantStack
- Jupyter Distinguished Contributor
- Jupyter Frontends SSC (Steering Software Council) representative
- Contributeur à de nombreux projets Jupyter
- Créateur de JupyterLite

</div>

---

# Les Jupyter Notebook

---

# L'écosystème Jupyter est très vaste

- Navigating the Jupyter Landscape
  - JupyterCon 2023 (Paris)
  - Jeremy Tuloup, Johan Mabille 
  - https://www.youtube.com/watch?v=uWJ0-OPKTxI

---

![bg fit 60%](img/repos_map.svg)

---

# JupyterLite

- Tout tourne dans le navigateur web via WebAssembly
- Se base sur la stack Jupyter existante:
  - Les noyaux Pyodide et Xeus executent le code dans le navigateur
  - JupyterLab et Jupyter Notebook
  - Voici pour faire des applications web et dashboards

---

![bg fit 60%](./img/jupyterlite.png)

---

![bg fit 75%](./img/jupyterlite.svg)

---

# Resources

- Jupyter Documentation: https://docs.jupyter.org
- This presentation: https://github.com/jtpio/alposs-2024

---

# Merci !

