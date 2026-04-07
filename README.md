# Was ist das?
Jupyter Notebooks für Sachverhalte aus van Steen: Distributed Systems.
Es ist einfach netter, den Code zum Ausführen und Demonstrieren zu haben, als ihn auf eine Powerpoint-Folie zu bannen.

Voraussetzungen:

```
pip install numpy matplotlib ipywidgets pandas
```
Optional: 
```
pip install jupyterlab
```

Start:
```
jupyter lab
```
oder
```
jupyter notebook
```
Dann Notebook öffnen und Code ausführen.

# Client-Server-Interaktion über Sockets
Einfache Demo mit Echo des Servers auf Anfrage des Clients.

[![Öffnen in Binder](https://mybinder.org/badge_logo.svg)](
https://mybinder.org/v2/gh/DanielBarie/jupyter_vansteen/main?labpath=vansteen_socketsClientServer.ipynb)

# Einfachere Sockets: ZeroMQ
Etwas Besseres als das einfache Berkely-Sockets-Modell.

## ZeroMQ Request-Reply-Pattern  
Request-Reply-Pattern. 

### Server startet vor Client  
[![Öffnen in Binder](https://mybinder.org/badge_logo.svg)](
https://mybinder.org/v2/gh/DanielBarie/jupyter_vansteen/main?labpath=vansteen_pyzmq_reqrepl.ipynb)

### Client startet vor Server  
[![Öffnen in Binder](https://mybinder.org/badge_logo.svg)](
https://mybinder.org/v2/gh/DanielBarie/jupyter_vansteen/main?labpath=vansteen_pyzmq_reqrepl_clientfirst.ipynb)

## ZeroMQ Publish-Subscribe-Pattern

### Ein Publisher, ein Subscriber
[![Öffnen in Binder](https://mybinder.org/badge_logo.svg)](
https://mybinder.org/v2/gh/DanielBarie/jupyter_vansteen/main?labpath=vansteen_pyzmq_pubsub.ipynb)

### Ein Publisher, zwei Subscriber (einer davon late)
[![Öffnen in Binder](https://mybinder.org/badge_logo.svg)](
https://mybinder.org/v2/gh/DanielBarie/jupyter_vansteen/main?labpath=vansteen_pyzmq_pubsub_latesub.ipynb)

## ZeroMQ Pipeline Pattern
[![Öffnen in Binder](https://mybinder.org/badge_logo.svg)](
https://mybinder.org/v2/gh/DanielBarie/jupyter_vansteen/main?labpath=vansteen_pyzmq_pipeline.ipynb)

# MPI

## einfache MPI-Demo
[![Öffnen in Binder](https://mybinder.org/badge_logo.svg)](
https://mybinder.org/v2/gh/DanielBarie/jupyter_vansteen/main?labpath=mpi_demo_python.ipynb)
