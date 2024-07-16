<div align=center>
  <img src="https://github.com/TempGROX/TempGROX/blob/main/src/photos/rounded-in-photoretrica.png" width="150">
</div>

<h1 align=center>my_og_validator_guide</h1>
This repository contains my guide to setting up the validator node of the OG_LABS project
<br>


# Download and Install
Before we begin, you should familiarize yourself with your network settings. I have compiled a convenient table for you, with which you can quickly familiarize yourself with these parameters :)

|PARAMETR|VALUE|
|:-------|:----|
|**Chain-Name**|0G-Newton-Testnet|
|**Chain-ID**|zgtendermint_16600-2|
|**Token-Name**|A0GI|
|**Chain-RPC**|https://rpc-testnet.0g.ai|
|**Chain-Websocket**|wss://rpc-testnet.0g.ai/ws|
|**Storage-RPC**|https://rpc-storage-testnet.0g.ai|

Great, now that you've reviewed these options, we can move on!

## System Requirements
Here are the minimum requirements for your system; if your computer is weaker than these mandatory requirements, then, alas, you will not succeed!

|SYSTEM PARAMETR|VALUE|
|:--------------|:----|
|**Memory**|64 GB|
|**CPU**|8 cores|
|**Disk**|1 TB NVME SSD|
|**BW**|100 MBps|

Great, now we can continue! I hope your computer meets the requirements)

## Install 0gchaind via CLI
```bash
git clone -b v0.2.3 https://github.com/0glabs/0g-chain.git
./0g-chain/networks/testnet/install.sh
source ~/.profile
```
### Set Chain ID
```bash
0gchaind config chain-id zgtendermint_16600-2
```

## Initialize Node
```
0gchaind init <your_validator_name> --chain-id zgtendermint_16600-2
```

## Download and validate the Genesis file
```bash
sudo apt install -y unzip wget
rm ~/.0gchain/config/genesis.json
wget -P ~/.0gchain/config https://github.com/0glabs/0g-chain/releases/download/v0.2.3/genesis.json
```
Validate:
```bash
0gchaind validate-genesis
```

## Add Seeds to `config.toml`
Seeds:
```bash
81987895a11f6689ada254c6b57932ab7ed909b6@54.241.167.190:26656,010fb4de28667725a4fef26cdc7f9452cc34b16d@54.176.175.48:26656,e9b4bc203197b62cc7e6a80a64742e752f4210d5@54.193.250.204:26656,68b9145889e7576b652ca68d985826abd46ad660@18.166.164.232:26656
```

## Start TestNet
```bash
0gchaind start
```

# The end!
If you liked this guide, please go to all my social networks)

<br>
<div id="badges" align="center">
  <a href="https://discord.com/users/961408999411048461">
    <img src="https://img.shields.io/badge/Discord-blue?style=for-the-badge&logo=https%3A%2F%2Fimg.icons8.com%2Fios%2F50%2Fmedium-logo.png&logoColor=white" alt="LinkedIn Badge"/>
  </a>
  <a href="https://medium.com/@James_Brandon">
    <img src="https://img.shields.io/badge/Medium-black?style=for-the-badge&logo=https%3A%2F%2Fimg.icons8.com%2Fios%2F50%2Fmedium-logo.png&logoColor=white" alt="Youtube Badge"/>
  </a>
  <a href="https://keybase.io/jamesbrandon">
    <img src="https://img.shields.io/badge/Keybase-orange?style=for-the-badge&logo=https%3A%2F%2Fimg.icons8.com%2Fios%2F50%2Fmedium-logo.png&logoColor=white">
  </a>
  <a href="https://x.com/JBTGrox">
    <img src="https://img.shields.io/badge/Twitter-blue?style=for-the-badge&logo=twitter&logoColor=white" alt="Twitter Badge"/>
  </a>
  <a href="https://linktr.ee/JBrandon_?utm_source=linktree_admin_share">
    <img src="https://img.shields.io/badge/Linktree-green?style=for-the-badge&logo=https%3A%2F%2Fimg.icons8.com%2Fios%2F50%2Fmedium-logo.png&logoColor=white">
  </a>
</div>
