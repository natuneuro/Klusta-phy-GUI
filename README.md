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
  - Deactivate the miniconda base environment **(optional)**
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
It is obtained a `.kwik` file that will be open with **phy GUI**

# phy GUI

phy is an open-source Python library providing a graphical user interface for visualization and manual curation of large-scale electrophysiological data. It is optimized for high-density multielectrode arrays containing hundreds to thousands of recording sites (mostly Neuropixels probes).

This software compile on Ubuntu 20.04

## Documentation

- [phy documentation](https://phy.readthedocs.io/en/latest/)

- [phy repository](https://github.com/cortex-lab/phy)

## Install guide

### Dependencies

Install the following dependencies before installing phy GUI

```
sudo apt install python3-pip
python3-is-python
```
  1. Install phy GUI
```
pip install phy klusta phycontrib --pre --upgrade
```
  2. PATH confinguration
  
Open `/home` directory and press `Ctl + H` to view hidden files, open `.bashrc` file and add the next line at the end of the file:
 ```
 export PATH = "~/.local/bin:$PATH"
 ```
  3. Done! Now, to use phy GUI, enter the directory that contains your files and type: 
```
phy kwik-gui file_name.kwik
```
  
