# Was ist das?
Jupyter Notebooks für Sachverhalte aus van Steen: Distributed Systems.
Es ist einfach netter, den Code zum Ausführen und Demonstrieren zu haben, als ihn auf eine Powerpoint-Folie zu bannen.

Voraussetzungen:

```
pip install numpy mpi4py impi-rt
```
JuyterLab: 
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
[Einfache Demo mit Echo des Servers auf Anfrage des Clients.](vansteen_socketsClientServer.ipynb)

[![Öffnen in Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/DanielBarie/jupyter_vansteen/main?labpath=vansteen_socketsClientServer.ipynb)

# Einfachere Sockets: ZeroMQ
Etwas Besseres als das einfache Berkely-Sockets-Modell.

## ZeroMQ Request-Reply-Pattern  
Request-Reply-Pattern in zwei Varianten:

- [Server startet vor Client](vansteen_pyzmq_reqrepl.ipynb)  
  [![Öffnen in Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/DanielBarie/jupyter_vansteen/main?labpath=vansteen_pyzmq_reqrepl.ipynb)
- [Client startet vor Server](vansteen_pyzmq_reqrepl_clientfirst.ipynb)  
  [![Öffnen in Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/DanielBarie/jupyter_vansteen/main?labpath=vansteen_pyzmq_reqrepl_clientfirst.ipynb)

## ZeroMQ Publish-Subscribe-Pattern
Zwei Varianten:

- [Ein Publisher, ein Subscriber](vansteen_pyzmq_pubsub.ipynb)  
  Braucht Fix: Threads nicht mit `daemon=True` starten (siehe Late Subscriber).  
  [![Öffnen in Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/DanielBarie/jupyter_vansteen/main?labpath=vansteen_pyzmq_pubsub.ipynb)

- [Ein Publisher, zwei Subscriber (einer davon late)](vansteen_pyzmq_pubsub_latesub.ipynb)  
  Hier ist Fix schon eingebaut.  
  [![Öffnen in Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/DanielBarie/jupyter_vansteen/main?labpath=vansteen_pyzmq_pubsub_latesub.ipynb)

## ZeroMQ Pipeline Pattern
[Auch bekannt als Consumer-Producer oder Push-Pull.](vansteen_pyzmq_pipeline.ipynb)  

[![Öffnen in Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/DanielBarie/jupyter_vansteen/main?labpath=vansteen_pyzmq_pipeline.ipynb)

# MPI

- [Einfache MPI-Demo](mpi_demo_python.ipynb)
  Jeder Prozess gibt seine eigene `rank` sowie die Gesamtzahl der Prozesse `size` aus. Keine direkte Ausführung des Codes im Notebook, enthält aber die Möglichkeit, den Demo-Code in eine Datei zu schreiben. Diese kann dann manuell ausgeführt werden.  
  Nicht ausführbar in Binder, da dort die MPI-Pakete fehlen. Zum Anschauen:  
  [![Öffnen in Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/DanielBarie/jupyter_vansteen/main?labpath=mpi_demo_python.ipynb)

- [Einfache MPI-Demo mit Ausführung im Notebook](mpi_notebook_exec.ipynb)
  MPI-Demo (s.o.) mit Ausführung des Codes direkt aus dem Notebook.  
  Nicht ausführbar in Binder, weil dort im Container die MPI-Pakete fehlen. Zum Anschauen:  
  [![Öffnen in Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/DanielBarie/jupyter_vansteen/main?labpath=mpi_notebook_exec.ipynb)

- [MPI-Demo Matrixmultiplikation](mpi_matrixmultiplikation_notebook.ipynb)
  Parallele Matrix-Vektor-Multiplikation mit MPI, direkte Ausführung des Codes im Notebook (wird in Datei geschrieben und jeweils als `subprocess` ausgeführt).
  Nicht ausführbar in Binder, weil dort im Container die MPI-Pakete fehlen. Zum Anschauen:   
  [![Öffnen in Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/DanielBarie/jupyter_vansteen/main?labpath=mpi_matrixmultiplikation_notebook.ipynb)
