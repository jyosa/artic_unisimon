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

5. Copie  los archivos del directorio artic_unisimon al directorio analysis

```
$ cp artic_unisimon/* .
```
6. Instale  el  programa guppy para realizar basecalling y barcode, la forma más sencilla es bajar el archivo de los repositorios de nanopore, descomprimir el archivo y luego usar los binarios:


```
$ GuppyBinary="https://mirror.oxfordnanoportal.com/software/analysis/ont-guppy_x.x.x_linux64.tar.gz"
$ wget GuppyBinary
$ tar -xzvf ont-guppy_X.X.X_linux64.tar.gz
```

Reemplace x.x.x por la version que requiera. Consulte la versión de cuda y drivers de la tarjeta  gráfica requeridos para correr guppy

7. Una  vez instalado abra el archivo config.py y remplace los  valores con los requeridos en su máquina
8. El script envía  un email una vez el proceo haya realizado, funcioina sólo con cuentas  de gmail, es recomendable  que abra unoexclusivamente para este propósito, no use su email personal o instituciional.
9. Si decide activar la función de envíar email una vez todo el proceso termina hay que darle autorización al correo de enviar email automáticos, para esto en el siguiente [link](https://myaccount.google.com/lesssecureapps?pli=1&rapt=AEjHL4NcmwjFrSP4rJSLCPYA5gs6GhVq_GuFa5RlI5i3w7fZM7vI-N36ssoEEyTcCbu4Vhe5q77aAoZQH58B9qWMlHBxdmkuxw). active la función de acceso de apps menos seguras. https://myaccount.google.com/lesssecureapps?pli=1&rapt=AEjHL4NcmwjFrSP4rJSLCPYA5gs6GhVq_GuFa5RlI5i3w7fZM7vI-N36ssoEEyTcCbu4Vhe5q77aAoZQH58B9qWMlHBxdmkuxw
