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

# Historique rapide de Jupyter

![bg fit right:30%](https://jupyter.org/assets/homepage/main-logo.svg)

---

# IPython dans le terminal

![fit](https://ipython.readthedocs.io/en/stable/_images/ipython-6-screenshot.png)

---

# REPL: Read Eval Print Loop

---

# Pourquoi les Jupyter Notebook sont populaires ?

- Le workflow REPL
- Avec en plus:
  - **narration**
  - **mémoire**
  - **reproductibilité**
  - **communication**

---

# IPython Notebook

![fit](https://user-images.githubusercontent.com/591645/228060329-13368066-b1e9-4812-9662-70919d833a77.png)

---

# Jupyter Notebook

![fit 90%](img/jupyter-notebook.png)

---

# JupyterLab

![fit 90%](img/jupyterlab.png)

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
  - Les noyaux Pyodide et Xeus exécutent le code dans le navigateur
  - Interfaces web JupyterLab et Jupyter Notebook
  - Voici pour faire des applications web et dashboards

---

![bg fit 60%](./img/jupyterlite.png)

---

![bg fit 75%](./img/jupyterlite.svg)

---

# Cas d'usage

---

![bg fit](https://github.com/jtpio/alposs-2024/assets/591645/de3ee8ac-5fbf-44e7-b76f-c97e9fb50218)

---

![bg fit](https://github.com/jtpio/alposs-2024/assets/591645/c0fe58fa-c2d8-4777-a996-9a8cd8f641f7)

---

# Un site Jupyter accessible en quelques secondes

---

# Education

---

# Ressources

- Documentation Jupyter: https://docs.jupyter.org
- Cette présentation: https://github.com/jtpio/alposs-2024

---

# Merci !
