<p align="center">
    <img height="100" height="auto" src="https://user-images.githubusercontent.com/56349947/205318364-965663f3-f9e4-4010-9e82-d4f5d29e9f4e.svg">
</p>
<h1 align='center'>Dusk Network</h1>
<p align='center'>Dusk Network is technology for securities. An open source and secure blockchain (DLT) infrastructure that businesses use to tokenize financial instruments and automate costly processes</p>
<p align='center'>
    <a href="https://dusk.network/">About Dusk Network</a>
</p>

# General Information

Tesnet Infomation :
> [Announcement](https://dusk.network/news/dusk-network-to-launch-rolling-incentivized-testnet-activities)

Official Guide Installation :
> [Guide](https://dusk.network/pages/incentivized-testnet)

# Requirement
To run node you must have meet a requirement:
## Minimum Hardware Requirement
|   CPU  | Memory | Disk  | Bandwith |
|--------|--------|-------|----------|
| 1 Core |  1 GB  | 25 GB | 100 Mbps |
## Software Requirement
- OS    : Ubuntu 22.04

# Manual Setup
For Install Manually Follow This Step

## Wallet Install
- Download CLI Wallet
```
wget https://github.com/dusk-network/wallet-cli/releases/download/v0.13.0/ruskwallet0.13.0-linux-x64-libssl3.tar.gz
tar -xvf tar -xf ruskwallet0.13.0-linux-x64-libssl3.tar.gz && mv ruskwallet0.13.0-linux-x64-libssl3 ruskwallet
cd ruskwallet
chmod +x rusk-wallet && ./rusk-wallet --state http://127.0.0.1:8585
```
- Create Wallet and Backup recovery phrase
<img src="https://lh5.googleusercontent.com/LtZ72tI1L_RXl29lAjxZzWMpuaF5xRqwmxm8EKkM4uhKi5MvbTjE2CNszKOVqS3r9RyU4uGnkIgRpEIKWuBJC_lwW9cpzkaEtwvG8uKag5cI0l-wevrZIABQqNkkaspP5XdcUKilDhB94UAFkcNdzRn0MFSdud2-MlhtLvJG49FD93jYSOnhLxaxWldRlw">
<img src="https://lh6.googleusercontent.com/zLBOd2yxH80CzL9-q-a_ELaKv9tlEMexSumGG4CCX4mMsNDCgk1bOe4Ppp1H7uzyg5ThSk6k2bK98UaJE2oWpAP_6ApO9uuRU7Y_5oK8wctrBexckRk_K871sFaqe75NFyHNHDRfBHt9heqzDffxtPME3DoLxopCdvSdxQAZ1wXr5Ffr1dzzHhL_yr6VNw">
- Select Address
<img src="https://lh6.googleusercontent.com/i-40brTLabk5nhxAThM_Q5iXe4SimGfdPnOKDvHbH7gUV_r4Zkn-i6Qm-O821eW80aRgWZhkUSTJwvgCnrC8KDf0oCrlHTMWvN4VYNRjJhdQp7PfwjG1j6kM6gbklom_aSt3sHAsi3p5dcNntZVEFNHC05UXlMcy3Y3ojXrD8gmfZi_fkXkVoVpL950EKw">
- Export provisioner key-pair and fill password to protect the file
<img src="https://lh4.googleusercontent.com/b-HsbMRGnDWnAVh4-NodBi8-0evB5jC_LhOLcQbsMrszWMqDKbZ03TD9lWGM651TzsxrZNFZ5yDBu5MAEdH5THulUM8cKAZ_T4UebAUU6JAb_fkXIxI_9FYJkpnvkwuyqKe6ISZqR2Gd8esi0Rl6zFywt-ZAK3S1ZiCogKWEt8wNevK0Clikq-lp_HcLTA">
and show these two file `.key & .cpk` when export success, backup the file in save place
<img src="https://lh6.googleusercontent.com/dPBSfyqf8GrS1MSi2DykX0tlGl1OR4cJmN6UYU2xs327QacO4YzROpunm2Lbnhe52q2jQOsCvrY6fCpa1xB33DZuPBFmMHZ5l66pYSZWKBFvVf2Ud1icA_wdbPxm9oXilvntXtassOoh2fZQLhP0sOxs5GxYnhWm-v8l4in-x-r5yhYMpknZSMt3Y-BLCQ">

<p align="center">
    <a href="https://forms.gle/3h4wDbab9f6bZ68L8" target="_blank">Fill the form to get Faucet</a>
</p>

## Node Install
### 1. Update 
```
sudo apt update && sudo apt upgrade -y 
```
### 2. Open Port
```
ufw allow 22
ufw allow 9000:9005/udp
ufw allow 8585
ufw enable
```
### 3. Set Up a Node
```
curl --proto '=https' --tlsv1.2 -sSf https://dusk-infra.ams3.digitaloceanspaces.com/rusk/itn-installer.sh | sh
```
### 4.
