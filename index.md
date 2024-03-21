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

# Jérémy Tuloup

- Directeur Technique à QuantStack
- Jupyter Distinguished Contributor
- Jupyter Frontends SSC (Steering Software Council) representative
- Contributeur à de nombreux projets Jupyter
- Créateur de JupyterLite

---

# Historique rapide de Jupyter

![bg fit right:30%](https://jupyter.org/assets/homepage/main-logo.svg)

---

# IPython dans le terminal

![fit](https://ipython.readthedocs.io/en/stable/_images/ipython-6-screenshot.png)

---

# REPL: Read Eval Print Loop

---

# Pourquoi les notebooks sont populaires ?

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

# LIGO

<div class="columns">


<div>
<img src="https://github.com/jtpio/alposs-2024/assets/591645/ebcf3de3-7e5e-43ec-87a4-c7cc19379680" />
</div>

<div>
<img src="https://github.com/jtpio/alposs-2024/assets/591645/2aa58b86-b9d8-437d-8153-345f00a73b08" />
</div>

</div>

---

# Black Hole M87

<div class="columns">

<div>
<img src="https://github.com/jtpio/alposs-2024/assets/591645/3600c6d4-1894-48f1-9855-4d760d53e84c">
</div>

<div>
<img src="https://github.com/jtpio/alposs-2024/assets/591645/c1cb7afe-0840-48b7-9708-67b5bd7fd0ff">

</div>

</div>

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
- ✅ pas de ligne de commande pour les utilisateurs
- ✅ pas besoin d'installer Python et autres paquets
- ✅ peut être hébergé comme site statique

---

# Un site Jupyter accessible en quelques secondes

![center h:600px](https://user-images.githubusercontent.com/591645/120649478-18258400-c47d-11eb-80e5-185e52ff2702.gif)

---

# Générateur de site statique

```shell
pip install jupyterlite-core

jupyter lite build
```

---

# Fichiers HTML, CSS, JavaScript, Wasm

<div class="columns">
<div>


```
├── api
│   └── translations
│       ├── all.json
│       └── en.json
├── bootstrap.js
├── build
│   ├── 9507.1e6cc5d.js
│   ├── 9602.62bf0f1.js
│   ├── 9621.e2e8b5d.js
│   ├── ...
│   ├── repl
│   │   ├── bundle.js
│   ├── retro
│   │   ├── bundle.js
│   ├── schemas
│   │   ├── all.json
│   │   ├── @jupyterlab
│   │   │   ├── application-extension
│   │   │   │   ├── commands.json
│   │   │   │   ├── context-menu.json
│   │   │   │   ├── shell.json
│   │   │   │   └── sidebar.json
│   ├── themes
│   │   └── @jupyterlab
│   │       ├── theme-dark-extension
│   │       │   ├── index.css
│   │       │   └── index.js
...
```
</div>
<div>

```
...
│   │       └── theme-light-extension
│   │           ├── index.css
│   │           └── index.js
├── config-utils.js
├── extensions
│       └── xeus-python-kernel
│           └── static
│               ├── numpy-1.24.2-py310h6d2fff6_0.0.data
│               ├── numpy-1.24.2-py310h6d2fff6_0.0.js
│               ├── python-3.10.2-h_hash_26_cpython.0.data
│               ├── python-3.10.2-h_hash_26_cpython.0.js
│               ├── python_data.js
│               ├── remoteEntry.35b4eac217ec6bf078a4.js
├── lab
│   ├── favicon.ico
│   ├── index.html
│   ├── jupyter-lite.ipynb
│   ├── jupyter-lite.json
│   ├── package.json
│   ├── tree
│   │   └── index.html
│   └── workspaces
│       └── index.html
...
```

</div>
</div>

---

# Cas d'usage

---

![center h:300px](https://user-images.githubusercontent.com/591645/162619390-ecab994a-3f39-4e26-af78-ca2569aee9b2.png)

```html
<iframe
  src="https://jupyterlite.github.io/demo/repl/index.html?kernel=python&toolbar=1"
  width="100%"
  height="500px"
>
</iframe>
```

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

- Capytale: https://capytale.fr
- Paris Saclay: https://jupyter.gitlab.dsi.universite-paris-saclay.fr/tutoriel-jupyter/utiliser.html
- UC Berkeley

---

# :rocket: Deployez sur GitHub Pages

- https://github.com/jupyterlite/demo

![center height:400px](https://raw.githubusercontent.com/jupyterlite/xeus-python-demo/main/deploy.gif)


---

https://jupyterlite.github.io/demo/


![](https://github.com/jtpio/alposs-2024/assets/591645/9e19fcea-4f17-4bd4-a83a-9eb548bd9968)

---

# 🔍 Références

- Documentation Jupyter: https://docs.jupyter.org
- Cette présentation:
  - Repo: https://github.com/jtpio/alposs-2024
  - Slides: https://jtp.io/alposs-2024

---

# Merci !
