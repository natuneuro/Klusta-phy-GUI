# Klusta

klusta is an open source software for automatic spike sorting. It has been designed to scale up to recordings made with probes containing a few dozen channels.

This softwaare compile on Ubuntu 20.04

## Documentation 

For more information about this software please read: 

- [klusta repository](https://github.com/kwikteam/klusta)

- [klusta documentation](https://klusta.readthedocs.io/en/latest/)

## Install guide

 1. Install Miniconda 
    
  - Download the latest shell script
```
wget https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh
```
  - Make the miniconda installation script executable
```
chmod +x Miniconda3-latest-Linux-x86_64.sh
```
  - Run miniconda installation script
```
./Miniconda3-latest-Linux-x86_64.sh
```
  - Deactivate the miniconda base environment 
```
conda config --set auto_activate_base false
```
  2. Download de environment file in this repository

  3. Create a virtual environment

```
conda env create -n klusta -f environment_klusta.yml
```
  4. Install kusta 
```
pip install klusta --upgrade 
```
  5. Done! Now, to use klusta, enter the directory that contains your files and type:
```
conda activate klusta # activate the klusta environment
klusta file_name.prm  # spikesort your data with a PRM file
```
It is obtained a `.kwik` file that is open with **phy GUI**
