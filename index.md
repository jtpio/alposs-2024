---
marp: false
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

![bg fit right:30%](https://jupyter.org/assets/homepage/main-logo.svg)

# Creer des sites Jupyter interactifs avec JupyterLite

## AlpOSS 2024

---

# About
<div>

## Jérémy Tuloup

- Technical Director at QuantStack
- Jupyter Distinguished Contributor
- Contributes to JupyterLab, Jupyter Notebook, Voilà
- Author of JupyterLite

</div>

---

![bg fit 60%](img/repos_map.svg)

---

# The Jupyter Interfaces

---

![center](img/web-apps.svg)

---

# JupyterLab

- Next-gen UI for Project Jupyter
- Allows to work with multiple notebooks, consoles, text editors, terminals, etc...
- Rich ecosystem of extensions
- Allows for custom lab-based applications
- Start with `jupyter lab`

![bg fit right](img/jupyterlab.png)

---

# Jupyter Notebook

- What users often call "Jupyter"
- The frontend is a web application
- Notebook 7 is built with JupyterLab components
- Start with `jupyter notebook`

![bg fit right](img/jupyter-notebook.png)

---

# Voilà

- Turn notebooks into standalone web applications
- Can be customized with templates and themes
- Start with `voila my_notebook.ipynb`

![bg fit right:40%](img/voila.png)


---

![center](img/all-web-apps.svg)

---

# nbconvert

- Convert notebooks to other formats
- Start with `jupyter nbconvert my_notebook.ipynb`
- Can also be used from the notebook UI

![bg fit right](img/nbconvert-export.png)

---

# The Jupyter Backends

---

![bg fit 60%](img/client_server_kernel-0.svg)

---

# Jupyter Server

- Backend to Jupyter Web applications (not the consoles):
    - core services
    - APIs
    - REST endpoints
- Client of kernels
- Responsible for launching and keeping kernels alive
- Use the same protocol for Web apps and kernels

---

# Servers

- Jupyter Server: historical, mono user, based on tornado
- Jupyverse: alternative implementation based on asyncio
- JupyterHub: multi-user server using Jupyter Server

---

![bg fit 60%](img/client_server_kernel-1.svg)

---

# Kernel protocol

- Documentation at https://jupyter-client.readthedocs.io/en/stable/messaging.html
- Agnostic to the language
- `jupyter_client` is the reference implementation in Python
- `xeus` is the reference implementation in C++
- Implementations rely on ZeroMQ

![bg fit right:30%](https://xeus.readthedocs.io/en/latest/_images/jupyter_archi.svg)

---

![bg fit 60%](img/client_server_kernel-2.svg)

---

# Kernels

- ipykernel, reference implementation of python kernel
- kernel wrapper approach (kernels based on ipykernel)
- standalone kernels (IJulia, IRKernel)
- xeus-based kernels (xeus-cling, xeus-python, xeus-lua, etc...)

---

# The Jupyter Widgets

---

![bg fit 60%](img/widgets.svg)

---

# Widgets

- ipywidgets / xwidgets: basic interactive widgets (sliders, buttons, checkboxes...)
- ipyleaflet / xleaflet: interactive maps based on leaflet
- bqplot / xplot: plotting libraries implementing the grammar of graphics
- many others ....

![bg fit right](img/widgets.png)

---

# JupyterLite

- WebAssembly powered Jupyter running in the browser
- Stands on the shoulder of giants:
  - Xeus kernels running in the browser
  - JupyterLab and Jupyter Notebook
  - Voici to turn notebooks into static web applications
  - Support for Jupyter Widgets and visualization libraries
- No real `jupyter-server`, `jupyter-client`, `nbconvert`

---

![bg fit 60%](./img/jupyterlite.png)

---

![bg fit 75%](./img/jupyterlite.svg)

---

# Resources

- Jupyter Documentation: https://docs.jupyter.org
- This presentation: https://github.com/JohanMabille/navigating-jupyter-landscape

---

# Thanks!

---

![bg fit 60%](img/repos_map.svg)

