## Creating Amazon EC2 Instance

go on amazon, make an account, initiate amazon ec2 Instance
download key to your computer from amazon
then move key to place where you usually store keys (ssh folder):

show what's inside folder (check make sure you have ssh folder):  
ls ~/.ssh

move key to ssh folder (have to be inside folder you've downloaded):
mv Keyname.pem ~/.ssh

Open text editor:
nano ~/.ssh/config
Added the Key into text editor for posterity's sake:
Host Keyname
    HostName [IPv4 Public IP -- grab from Amazon EC2 Description]
    User root
    IdentityFile ~/.ssh/Keyname.pem
Exit Nano text editor (control X)

Change permissions of key so that it's private (Amazon needs it to be that way):
chmod 400 ~/.ssh/Jenna.pem

access amazon EC2
Grab Public DNS (IPv4) from Description of Instance on Amazon:
ssh -i ~/.ssh/Keyname.pem ubuntu@[Public DNS (IPv4)]

##Uploading Files to EC2

scp -i ~/.ssh/Keyname.pem  ~/ImageLocation ubuntu@[Public DNS (IPv4)]

##Add memory to EC2 (create swap-file)

sudo fallocate -l 1G /swapfile
sudo chmod 600 /swapfile
sudo mkswap /swapfile
sudo swapon /swapfile
free -h

##Put Python in EC2

- EC2 needs Python cause Kraken is in Python

(double check later, this is probably redundant)

sudo curl https://bootstrap.pypa.io/get-pip.py | python
curl -O https://bootstrap.pypa.io/get-pip.py
python3 get-pip.py --user
sudo apt-get install python-pip
sudo apt-get update
sudo apt-get install python-pip
sudo pip install numpy

 
