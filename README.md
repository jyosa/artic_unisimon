# Artic-ncov2019 Automatización

Este program escrito en python le permite correr  el protocolo artic-ncov2019 completo de forma sencilla.


## Antes de empezar

Aates de empezar asegurese de que el ambiente artic-ncov2019 este instalado con todas las dependencias necesarias, para hacerlo realice lo siguiente:

1. Instale  [conda y mininiconda](https://docs.conda.io/projects/conda/en/latest/user-guide/install/linux.html).
2. Bajar e instalar el pipeline artic-ncov2019:

```
$ git clone https://github.com/artic-network/artic-ncov2019.git
$ cd artic-ncov2019
$ conda env remove -n artic-ncov2019
$ conda env create -f environment.yml
```
Lo anterior crea un ambiente llamado artic-ncov2019

Nota!!! conda tiene un bug que  revisa una y otra vez diferentes canales haciendo que el proceso de instalación dure por lo menos  9 horas!!!!!! no desespere déjelo instalando en la noche.

3. Cambie de directorio a $HOME/artic-ncov2019 y genere un nuevo directorio llamado analysis:


```
$ cd $HOME/artic-ncov2019
$ mkdir analysis
```

4. Ingrese al directorio  analysis y clone el git de artic_unisimon

```
$ cd analysis
$ git clone https://github.com/jyosa/artic_unisimon.git

```
