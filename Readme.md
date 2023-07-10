# Net Tools 

the aim of this role is to provide the configuration of a vm that will provide several tools for network administration such as dns, dhcp, vpn. 
It could also provide storage endpoints over networks for any backup.

## Environment

First, the conda environment needs to be set-up. Download installation script from the repository: https://github.com/conda-forge/miniforge

Install miniforge and create environment by running:
'''
conda env create -f environment.yaml
'''

NOTE:
For security purposes, it could be good to install miniforge in a root owned directory (eg: /opt/miniforge3):
'''
sudo bash Miniforge3-Linux-x86_64.sh -b -p /opt/miniforge3
'''

Then create a group and change ownerships of envs folder:
'''
sudo groupadd condaenv
sudo chown -R root:/opt/miniforge3/envs
sudo chmod -R 775 /opt/miniforge3/envs
'''

Finally add the users that need access to conda envs:
'''
sudo usermod -aG condaenv user
'''
