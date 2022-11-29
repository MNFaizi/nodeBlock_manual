<p align="center">
    <img height="100" height="auto" src="https://user-images.githubusercontent.com/56349947/204550860-ecf49956-0283-4989-9b59-2469d7413ca7.svg">
</p>
<h1 align='center'>Power DCloud</h1>
<p align='center'><b>Power DCloud</b> is the world’s first DeInfra, which completely beats the problem of inability to build really decentralized dApps without centralized parts or the necessity to use centralized services.</br>
Based on blockchain platform DCloud combines a universal set of services: multi virtual machines, decentralized storage, sophisticated tokenomisc, nodes and chains, with Power Hub as one-stop entry for developers, users, node providers and projects.
</p>
<p align='center'>
    <a href="https://doc.thepower.io/docs/about"></a>Official Documentation About Power DCloud (DeInfra)
</p>

# General Information

> [About Testnet](https://medium.com/the-power-official-blog/deinfra-testnet-verification-and-test-assignment-in-the-community-bot-are-launched-today-b253f397b1fa)

> [Telegram Groub](https://t.me/thepower_chat)

> [Telegram Announcement](https://t.me/thepowerio)

> [Rover Bot](https://t.me/thepowerio_bot)

> [Checker](https://zabbix.thepower.io/zabbix.php?action=dashboard.view#)

# Requirement
To run node you must have meet a requirement:
## Minimum Hardware Requirement
- CPU       : 4 Core
- Memory    : 4 GB
- Disk      : 40 GB
- Bandwith  : 100 Mbps

## Software Requirement
- OS        : Ubuntu 22.04 Desktop
- Erlang    : 24.3 Version
- Docker    : 20.10.18 Version

# Manual Setup
For install manually follow this step

## 1. Choose installation method

| Install Method |               Manual             |
|----------------|----------------------------------|
|     Docker     | [click here](./DockerInstall.md) |
|   Source Code  | [Click here](./SourceInstall.md) |

## 2. Send Address to Rover_Bot for join waitlist

> [Rover Bot](https://t.me/thepowerio_bot)

`start bot` and follow step by step until you get into waitlist

> Format send to rover bot `http://YourDomain:YourPortNumber/api/node/status`

Wait until receive personal token to join tea Ceremony

## 3. Join Tea Ceremony
```
wget https://tea.thepower.io/teaclient
chmod +x teaclient
./teaclient -n <nickname> <chain token>.<personal token>

```
- 'nickname' change with your nickname
- 'chain token' get from dev it will publish in announcement channel<a href='https://t.me/thepowerio)'>Telegram Announcement</a>
- 'personal token' get from rover bot <a href="https://t.me/thepowerio_bot)">Rover Bot</a>

It wil generate 2 file `node.confg and genesis.txt` in your folder when you run tea client

> if you got the file continue to next step

## Run the node
```

```


