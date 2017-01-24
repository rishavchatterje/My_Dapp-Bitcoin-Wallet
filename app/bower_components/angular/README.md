My-First-Dapp
It has been made by using modern technologies or framework named Truffle and 
the use of Web3.js  really proved to be instrumental in completing this project.

Install Instructions

Developing for Ethereum is sometimes frustrating, because things change at fast pace. If something does not work as described here, please:

try a google search as you are 100% not alone with your problem
inform the instructors of the course so they can correct the problem
if you have the time, it would be awesome if you'd make a pull-request here
Windows

Download Pyhton: https://www.python.org/downloads/release/python-2712/

.Net Packages https://www.microsoft.com/en-US/download/details.aspx?id=49982

https://www.microsoft.com/en-us/download/details.aspx?id=30653

SSL https://slproweb.com/products/Win32OpenSSL.html

and eventually you also need the Visual Studio, because of the C++ Compiler: https://www.visualstudio.com/vs/

After downloading the Visual Studio make sure to open one time a new c++ project.

Install the Git-Bash as it comes with a mingw: https://git-scm.com/downloads

Install NodeJS and the Node Package Manager (NPM) https://nodejs.org/en/download/

Ubuntu

Install necessary packages:
sudo apt-get update && sudo apt-get upgrade
sudo apt-get install curl git vim build-essential
Install NodeJS and NPM
 curl -sL https://deb.nodesource.com/setup_6.x | sudo -E bash -
 sudo apt-get install -y nodejs
 sudo npm install -g express
Other Necessary Files

Download the Genesis File either from here or directly from the go-ethereum github page. It is advised to take it directly from the official github page, as it is probably more up to date.

Run the Project

On any OS you need Truffle

npm install -g truffle

and then clone this repository
git clone https://github.com/rishavpiku/My-First-Dapp.git

and run
bower install

which installs the angular components.

Additionally you need to have a geth node running (or the ethereumjs-testrpc), then you can simply:

truffle migrate
and

truffle build
or

truffle serve
which opens an HTTP Server on http://localhost:8080


Known Problems 

1.Geth Attach- On Windows its simply possible to do a geth attach, but on MacOS it seems that you need to provide the actual ipc file. geth --datadir /media/user/sdcard/chaindata --ipcpath $HOME/.ethereum/geth.ipc console

2.Private Network

The way the private network is initialized changed in the past months and seems to keep changing. For better information on it, it is advised to directly see the correct instructions on: https://github.com/ethereum/go-ethereum

Usually it should work with:

geth init path/to/genesis.json --datadir=/path/to/some/folder

