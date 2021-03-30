# How to originate a contract
## Set-up your environment
### Required environment variables
1. In the folder "config", create (or open it if you already have one!) your local file called `"prod.env"`
2. Add or update the required variables to your .env file:
```
#################################
# signer (smart contract owner) #
#################################

SIGNER_EMAIL=
SIGNER_PASSWORD=
SIGNER_MNEMONIC=
SIGNER_SECRET=
ADDRESS=

##################
# smart contract #
##################
RPC_ADDRESS=
SUPPLY=
```

### Required libraries
Node 14 or higher is required to run the originate function. 

#### Install node on MAC
1. Go to https://nodejs.org/en/download/ and choose "macOS Installer".
2. Follow the instructions on the wizard. 
3. Once it is complete, to check that the installation was successful, run:

``` bash
node -v
npm -v
```

#### Install node on Linux
1. Open your terminal, and run:
``` bash
sudo apt update
sudo apt install nodejs npm
```

2. Once it is complete, to check that the installation was successful, run:

``` bash
node -v
npm -v
```

### Clone the project from git
In order to clone the project from git, please run:
``` bash
# If you do not have an SSH key
git clone -b develop https://github.com/Smart-Chain-git/SmartLink-ICO.git

# If you have an SSH key
git clone -b develop git@github.com:Smart-Chain-git/SmartLink-ICO.git
```

### Install dependencies
1. Go to your project directory
``` bash
cd SmartLink-ICO
```
2. To install the dependencies, run:
``` bash
npm install
```

## Let's originate the contract!
1. Export your prod environment variables:
``` bash
export NODE_ENV=prod
```
2. Check that the env variable was set
``` bash
echo $NODE_ENV
```

3. At the root of your project, run:
``` bash 
npm run originate
```