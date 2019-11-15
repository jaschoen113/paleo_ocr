## Create an Amazon EC2 Instance

Once you've uploaded image files to Kraken and saved your transcriptions, you're ready to train the system. Training takes a long time to run, so instead of letting your own computer run the training in the background, or acquiring another computer just for this task, you can set up a virtual machine which will run the program remotely. Amazon offers various EC2 Instances (virtual servers) and the first year is free.

To create an Amazon EC2 Instance, first go to [Amazon Web Services](https://aws.amazon.com/?nc2=h_lg).

Next, create an account.

Once you have an account, navigate to [Launch a Virtual Machine](https://us-east-2.console.aws.amazon.com/ec2/v2/home?region=us-east-2#LaunchInstanceWizard:).

At Step 1 "Choose AMI," select "Amazon Linux." This is the free-tier virtual machine, and it's Linux, which is the operating system Kraken runs on.

At Step 2 "Choose an Instance Type," select the default, free-tier eligible General Purpose instance type.

For Steps 4 "Add Storage," 5 "Add Tags," and 6 "Configure Security Group," you can keep the default settings. [look over what we did for security settings]

Hit "Launch." [go through this entire process again to double check, and at what point you name things]

Now, you want to access this virtual machine from your own computer. To do so, first download the key from your instance to your computer. The "key" is basically a password that allows your computer access to the virtual machine. [this should be a pop-up when you launch it?]

It doesn't matter where you save this key at first, because we're gonna move it to a secure place in your computer after you've downloaded it. Once you've downloaded the key, open your terminal. In the command line, first check to make sure you have an ssh folder:

`ls ~/.ssh`

If you don't have an ssh folder, create one:

[how?]

Next, move the key to your ssh folder (replace "Keyname" with your actual key's name):

`mv Keyname.pem ~/.ssh`

Now we want to save the location of the key. In the command line, open a text editor (called Nano):

`nano ~/.ssh/config`

In the text editor, paste the following text, and replace the bracketed information with your key-specific information (make sure you remove brackets). To find the IPv4 for your EC2, navigate to Amazon's EC2 Dashboard and the specific instance you've launched (this should be open in your browser still). Under the "Description" tab, you'll find "IPv4 Public IP." Grab that number and paste it:

>Host [Keyname]  
HostName [IPv4 Public IP]  
User root  
IdentityFile ~/.ssh/[Keyname].pem

Exit the Nano text editor with ctrl-X

Now, we want to change the permissions of the key so that it's private (Amazon requires this) In the command line, enter:

`chmod 400 ~/.ssh/Jenna.pem`

Finally we're ready to access your instance from the terminal. Once again, enter your specific Key name and Public DNS (IPv4) (without brackets):

`ssh -i ~/.ssh/Keyname.pem ubuntu@[Public DNS (IPv4)]`

## Add memory to EC2

These commands create a "swap-file" which allows you to add more memory to your EC2 instance.

`sudo fallocate -l 1G /swapfile`  
`sudo chmod 600 /swapfile`  
`sudo mkswap /swapfile`   
`sudo swapon /swapfile`  
`free -h`  

## Put Python in EC2

Now that you've launched your virtual machine, you'll need to install Kraken (just as you did on your own computer). Since Kraken runs in Python, and the virtual machine does not come with Python automatically, you'll need to download Python first:

[double check later, this is probably redundant]

`sudo curl https://bootstrap.pypa.io/get-pip.py | python`  
`curl -O https://bootstrap.pypa.io/get-pip.py`  
`python3 get-pip.py --user`  
`sudo apt-get install python-pip`  
`sudo apt-get update`  
`sudo apt-get install python-pip`  
`sudo pip install numpy`  

## Upload Files to EC2

Once you've downloaded Kraken, you can use it as you would from your own computer. But remember that you're working in a virtual machine now, not your own computer. So any files on your computer are not in this virtual machine. So you have to manually upload files to the virtual machine, and then access them through Kraken. [we'll have to check whether this is true, since we might be able to upload stuff to Kraken on our own computers and then just run the training on Kraken?]. Again, replace Keyname and Public DNS with your instance-specific information. For "Image Location," you need the full location of the file. A quick way to find this location is to drag and drop your image (or file) to the terminal:   

`scp -i ~/.ssh/Keyname.pem  ~/ImageLocation ubuntu@[Public DNS (IPv4)]`
