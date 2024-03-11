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

https://jtp.io/alposs-2024

---

# About
<div>

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

![bg fit](https://raw.githubusercontent.com/jupyterlite/jupyterlite/main/docs/_static/icon.svg)

---

# JupyterLite

- Tout tourne dans le navigateur web via WebAssembly
- Se base sur la stack Jupyter existante:
  - Les noyaux Pyodide et Xeus exécutent le code dans le navigateur
  - Interfaces web JupyterLab et Jupyter Notebook
  - Voici pour faire des applications web et dashboards

---

# Jupyter

![center](https://user-images.githubusercontent.com/591645/228267004-e4e2e54f-1d5f-45b7-bacb-6c3a1844c479.png)

---

# JupyterLite

![center](https://user-images.githubusercontent.com/591645/237059523-d29b94e6-7287-4608-b617-b0fe2a74877a.png)

---


![bg fit 60%](./img/jupyterlite.png)

---

![bg fit 75%](./img/jupyterlite.svg)

---

# Jupyter et Python dans le navigateur

![center w:512](https://raw.githubusercontent.com/jupyterlite/jupyterlite/main/docs/_static/badge-launch.svg)

- ✅ pas de serveur Python
- ✅ pas de ligne de commande
- ✅ pas besoin d'installer Python et autres paquets
- ✅ peut être hébergé comme site statique

---

# Un site Jupyter accessible en quelques secondes

![center h:600px](https://user-images.githubusercontent.com/591645/120649478-18258400-c47d-11eb-80e5-185e52ff2702.gif)

---

# Cas d'usage

---

![bg fit](https://github.com/jtpio/alposs-2024/assets/591645/de3ee8ac-5fbf-44e7-b76f-c97e9fb50218)

---

![bg fit](https://github.com/jtpio/alposs-2024/assets/591645/c0fe58fa-c2d8-4777-a996-9a8cd8f641f7)

---

<video
  controls
  width="100%"
  height="600px"
  src="https://github.com/jtpio/alposs-2024/assets/591645/9b5e247d-cb89-4b15-aba3-97e5ab381bb5">
</video>

---

# Education

- Capytale
- Paris Saclay
- UC Berkeley

---

# :rocket: Deployez sur GitHub Pages

- https://github.com/jupyterlite/demo

![center height:400px](https://raw.githubusercontent.com/jupyterlite/xeus-python-demo/main/deploy.gif)


---

# 🔍 Références

- Documentation Jupyter: https://docs.jupyter.org
- Cette présentation:
  - Repo: https://github.com/jtpio/alposs-2024
  - Slides: https://jtp.io/alposs-2024

---

# Merci !
