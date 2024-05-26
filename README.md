

<p align="center">
  <img src="https://github.com/anuragbejju/FoodLedger/blob/main/docs/imgs/FoodLedger%20Logo.png" width="70" title="hover text" align="left">
</p>

# FoodLedger (Using ICP - Kybra)
FoodLedger uses decentralized collaboration services offered by ICP (Internet Computer Protocol) to facilitate seamless communication and coordination among stakeholders, ensuring efficient resource allocation and effective response to community needs.

### Dependencies
Follow the instructions exactly as stated below to avoid issues.
You should be using a *nix environment (Linux, Mac OS, WSL if using Windows) with bash and have the following installed on your system:

- Python 3.10.7
- dfx 0.19.0
- Python VS Code Extension
- Python 3.10.7
It is highly recommended to install Python 3.10.7 using pyenv. To do so, use the pyenv installer as shown below:

##### install pyenv
```'
curl https://pyenv.run | bash
````


##### install Python 3.10.7
````
~/.pyenv/bin/pyenv install 3.10.7
````

dfx
Run the following command to install dfx 0.19.0:
````
DFX_VERSION=0.19.0 sh -ci "$(curl -fsSL https://sdk.dfinity.org/install.sh)"
````
If after trying to run dfx commands you encounter an error such as dfx: command not found, you might need to add $HOME/bin to your path. Here's an example of doing this in your .bashrc:
````
echo 'export PATH="$PATH:$HOME/bin"' >> "$HOME/.bashrc"
````


### Execution

create and source a virtual environment:
````
~/.pyenv/versions/3.10.7/bin/python -m venv venv
source venv/bin/activate
````

Now install Kybra:
````
pip install kybra
````

Go inside FoodLedger folder and deploy

### Local deployment
Let's deploy to our local replica.

First startup the replica:

````
dfx start --background
````
If you want an extra speedy deploy:

````
dfx start --background --artificial-delay 0
````
Then deploy the canister:

````
dfx deploy
````


### Interacting with your canister from the web UI
After deploying your canister, you should see output similar to the following in your terminal:
````
Deployed canisters.
URLs:
  Backend canister via Candid interface:
    kybra_hello_world: http://127.0.0.1:8000/?canisterId=ryjl3-tyaaa-aaaaa-aaaba-cai&id=rrkah-fqaaa-aaaaa-aaaaq-cai
````


### Credits
This code and documentation is referenced from https://demergent-labs.github.io/kybra/the_kybra_book.html




