# Simple R installation

Simple instructions for installing R from source code on a linux os.

The following steps should be done in the bash terminal.

Example with version 4.1.0:

```bash
## First, you must download the R<version>.tar.gz file and decompress it.
wget https://cran.itam.mx/src/base/R-4/R-4.1.0.tar.gz
tar -zxvf R-4.1.0.tar.gz
cd R-4.1.0

## Then, configure and make
./configure --with-cairo --enable-R-shlib --with-blas --with-lapack
make
make check
make pdf
make info

## Finally, add symbolic links for the R and Rscript binaries with sudo
sudo ln -s ~/Apps/R-4.2.1/bin/R /usr/local/bin/R 
sudo ln -s ~/Apps/R-4.2.1/bin/Rscript /usr/local/bin/Rscript
```

