<p align="center">
    <img height="100" height="auto" src="https://user-images.githubusercontent.com/56349947/206959347-39000801-f2e7-464e-9d60-2a9e25df1306.png">
</p>
<h1 align='center'>Q Blockchain</h1>
<p align='center'>Q is a novel blockchain that combines the benefits of a public, open and decentralized ledger with the transparency and predictability of enforceable private contracts, thereby enabling adoption by a great variety of use cases that desire decentralization but require scalability and dependability.</p>
<p align='center'>
    <a href="https://q.org">Q Blockchain Website</a>
</p>
<p align="center">Q Blockchain Social Media</p>
<div align="center">
    <a href="https://discord.gg/YTgkvJvZGD" target="_blank"><img src="https://user-images.githubusercontent.com/50621007/176236430-53b0f4de-41ff-41f7-92a1-4233890a90c8.png" width="30"></a>
    <a href="https://twitter.com/QBlockchain" target="_blank"><img src="https://user-images.githubusercontent.com/56349947/205331052-6d4d4216-3529-490c-a1b9-8c3618aac8e2.png" width="30"></a>
</div>

# General Information

- Incentive Information :
>[Incentive Info](https://medium.com/q-blockchain/q-blockchain-validator-onboarding-program-part-1-validator-incentivized-testnet-567ef6e4002e)

- Official Guide :
>[Guide](https://docs.qtestnet.org/)

- Validator Status :
>[Validator](https://stats.qtestnet.org/)

# Requirement
To run node you must have meet a requirement:
> base on my machine
## Minimum Hardware Requirement
|   CPU  | Memory  |  Disk  | Bandwith |
|--------|---------|--------|----------|
| 8 Core |  32 GB  | 500 GB | 100 Mbps |
## Software Requirement
- OS    : Ubuntu 20.xx

# Manual Setup Validator Node
For Install Manually Follow This Step

## Update Dependency
```
sudo apt update && sudo apt upgrade -y
```
## install Docker
>you can skip this if have docker in your machine
```
sudo apt-get update && sudo apt install jq && sudo apt install apt-transport-https ca-certificates curl software-properties-common -y && curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add - && sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu focal stable" && sudo apt-get install docker-ce docker-ce-cli containerd.io docker-compose-plugin && sudo apt-get install docker-compose-plugin
sudo apt-get install docker-compose
```
## Clone the Repository
```
git clone https://gitlab.com/q-dev/testnet-public-tools
```
move to testnet-validator directory
```
cd testnet-public-tools/testnet-validator
```
## Generate Keypair for Validator
- Set vars password
```
QPASSWORD=YourPassword
```
`YourPassword` - change with your password
- export vars to .bash_profile
```
echo "export QPASSWORD=$QPASSWORD" >> $HOME/.bash_profile
source $HOME/.bash_profile
```
- create keystore directory and pwd.txt file
```
mkdir keystore
cd keystore
echo "QPASSWORD" >> pwd.txt
```
- generate new wallet
```
cd ..
docker-compose run --rm --entrypoint "geth account new --datadir=/data --password=/data/keystore/pwd.txt" testnet-validator-node
```
>after that you will see output command that your new key was generated like this
```
Your new key was generated

Public address of the key:   0xb3FF24F818b0ff6Cc50de951bcB8f86b52287dac
Path of the secret key file: /data/keystore/UTC--2021-01-18T11-36-28.705754426Z--b3ff24f818b0ff6cc50de951bcb8f86b52287dac

- You can share your public address with anyone. Others need it to interact with you.
- You must NEVER share the secret key with anyone! The key controls access to your funds!
- You must BACKUP your key file! Without the key, it's impossible to access account funds!
- You must REMEMBER your password! Without the password, it's impossible to decrypt the key!
```