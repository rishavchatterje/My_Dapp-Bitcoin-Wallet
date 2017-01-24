# Final DApp
This is the final DApp you are going to develop in the Etheruem Class.

## Scope
The scope of the DApp is to show the usage of Truffle, 

* demonstrate how to work with the Ethereum Blockchain 
* Web3 
* Listen and react to specific events
* Write Test Cases
* Deploy the DApp
* Work with MIST
* Integrate Angular into Truffle

## Install Instructions

Developing for Ethereum is sometimes frustrating, because things change at fast pace. If something does not work as described here, please:

1. try a google search as you are 100% not alone with your problem
2. inform the instructors of the course so they can correct the problem
3. if you have the time, it would be awesome if you'd make a pull-request here

### Windows

1. Download Pyhton:
 https://www.python.org/downloads/release/python-2712/

2. .Net Packages
 https://www.microsoft.com/en-US/download/details.aspx?id=49982

 https://www.microsoft.com/en-us/download/details.aspx?id=30653

3. SSL
 https://slproweb.com/products/Win32OpenSSL.html

4. and eventually you also need the Visual Studio, because of the C++ Compiler:
 https://www.visualstudio.com/vs/

 After downloading the Visual Studio make sure to open one time _a new c++ project_.

5. Install the Git-Bash as it comes with a mingw:
 https://git-scm.com/downloads

6. Install NodeJS and the Node Package Manager (NPM)
 https://nodejs.org/en/download/


### Ubuntu

1. Install necessary packages:
```
sudo apt-get update && sudo apt-get upgrade
sudo apt-get install curl git vim build-essential
```

2. Install NodeJS and NPM
```
 curl -sL https://deb.nodesource.com/setup_6.x | sudo -E bash -
 sudo apt-get install -y nodejs
 sudo npm install -g express
```


### Other Necessary Files

Download the Genesis File either from [here](genesis.json) or directly from the [go-ethereum github page](https://github.com/ethereum/go-ethereum#operating-a-private-network). It is advised to take it directly from the official github page, as it is probably more up to date.

## Run the Project

On any OS you need Truffle

```
npm install -g truffle
```

and then **clone this repository**
```
git clone https://github.com/tomw1808/truffle_eth_class1.git
```
and run

```
bower install
```

which installs the angular components.

Additionally you need to have a geth node running (or the ethereumjs-testrpc), then you can simply:

```
truffle migrate
```

and

```
truffle build
```

or

```
truffle serve
```

which opens an HTTP Server on http://localhost:8080

## Known Issues

### Geth Attach

https://www.udemy.com/ethereum-developer/learn/v4/questions/1846724

On Windows its simply possible to do a `geth attach`, but on MacOS it seems that you need to provide the actual ipc file. `geth --datadir /media/user/sdcard/chaindata --ipcpath $HOME/.ethereum/geth.ipc console` which is a problem posed here: http://ethereum.stackexchange.com/questions/4472/port-30303-error-in-mist-when-i-run-geth-with-a-different-datadir


### Private Network
The way the private network is initialized changed in the past months and seems to keep changing. For better information on it, it is advised to directly see the correct instructions on:
https://github.com/ethereum/go-ethereum

_Usually_ it should work with:
```
geth init path/to/genesis.json --datadir=/path/to/some/folder
```


### Solidity Compilation Errors/Warnings
Solidity is in active maintenance and things change _all the time_! The code throughout the course was written for SolC 3.5, the current version (at the time this Readme was written) is 0.4.8.

Any Solidity Program can be "forced" to use another compiler version (older one) by using as _first line in your program_
`pragma solidity ^0.4.0;` for version 0.4.0, change it to whatever version you might need.

The code here is updated to work with solidity 0.4.8.


## Contact
If you run into any problems, don't hesitate to contact us on the course-forum at any time. If you use the forum-search function, there is a high chance that you find the answer to your problem already.
