[![Github All Releases](https://img.shields.io/github/downloads/xmrig/xmrig/total.svg)](https://github.com/diamonds-miner/diamonds/releases)
[![GitHub release](https://img.shields.io/github/release/xmrig/xmrig/all.svg)](https://github.com/diamonds-miner/diamonds/releases)
[![GitHub Release Date](https://img.shields.io/github/release-date/xmrig/xmrig.svg)](https://github.com/diamonds-miner/diamonds/releases)

![Без имени](https://user-images.githubusercontent.com/75134782/100481307-be768280-3104-11eb-8fdc-554fbf0da807.png)

## Miner for ETH, BTM, SERO, HNS, BFC

## Performance (stock frequency)

| Algorithm        |  Coin   |  P106-100  |  P104-8G   |   1070ti   |  1080ti  |   2080   | RX580 2048sp |
| :--------------- | :-----: | :--------: | :--------: | :--------: | :------: | :------: | :----------: |
| tensority        |   BTM   |   1,900    |    3000    |   3,400    |  5,000   |  11,500  |      X       |
| ethash           |   ETH   |   21.2M    |   34.5M    |   26.9M    |   46M    |  35.5M   |     24M      |
| tensority_ethash | BTM+ETH | 950+15.5M  | 1600+26.5M |  1350+22M  | 2450+40M | 7000+28M |      X       |
| progpow_sero     |  SERO   |   10.3M    |   17.5M    |   13.3M    |  22.5M   |  25.8M   |     10M      |
| bfc              |   BFC   |     80     |    130     |    120     |   190    |   210    |      X       |
| hns              |   HNS   |    170M    |    255M    |    300M    |   455M   |   425M   |     145M     |
| hns_ethash       | HNS+ETH |  76M+19M   |  120M+30M  | 158M+26.2M | 176M+44M | 305M+34M |  68M+22.5M   |

## Features

* Support Windows.
* Support backup mining pool configuration.
* Support SSL connection to mining pools.
* Dev Fee: 1%

## Requirements

- **NVIDIA Driver version: >= 377**.
- GPU Specific Requirements:

| Algorithm        |  Coin   | Compute Capability | Memory (Win7 & Linux) | Memory (Win10) |
| :--------------- | :-----: | :----------------: | :-------------------: | :------------: |
| tensority        |   BTM   |   6.1, 7.0, 7.5,8.0, 8.6   |          1GB          |      1GB       |
| ethash           |   ETH   | 6.0, 6.1, 7.0, 7.5, 8.0,8.6 |          4GB          |      4GB       |
| tensority_ethash | BTM+ETH | 6.1, 7.0, 7.5, 8.6 |          4GB          |      4GB       |
| progpow_sero     |  SERO   | 6.0, 6.1, 7.0, 7.5, 8.0,8.6 |          2GB          |      2GB       |
| bfc              |   BFC   | 6.0, 6.1, 7.0, 7.5, 8.0,8.6 |          5GB          |      6GB       |
| hns              |   HNS   | 6.0, 6.1, 7.0, 7.5, 8.0,8.6 |         0.1GB         |     0.1GB      |
| hns_ethash       | HNS+ETH | 6.0, 6.1, 7.0, 7.5, 8.0,8.6 |          4GB          |      4GB       |
| beamv3 | BEAM | 6.0, 6.1, 7.0, 7.5 | 3GB | 3GB |
| octopus | CFX | 6.0, 6.1, 7.0, 7.5, 8.0,8.6 | 5GB | 5GB |

- \* Compute Capability reference link: [wikipedia](<https://en.wikipedia.org/wiki/CUDA#GPUs_supported>)

## Sample Usages

#### BTM

- **f2pool:** nbminer -a tensority -o stratum+tcp://btm.f2pool.com:9221 -u bm1xxxxxxxxxx.worker
- **antpool:** nbminer -a tensority -o stratum+tcp://stratum-btm.antpool.com:6666 -u username.worker
- **matpool.io:** nbminer -a tensority -o stratum+tcp://btm.matpool.io:8118 -u bm1xxxxxxxxxxx.worker

#### ETH

- **ethermine:** nbminer -a ethash -o ethproxy+tcp://asia1.ethermine.org:4444 -u 0x12343bdgf.worker
- **sparkpool:** nbminer -a ethash -o ethproxy+tcp://cn.sparkpool.com:3333 -u 0x12343bdgf.worker
- **f2pool:** nbminer -a ethash -o ethproxy+tcp://eth.f2pool.com:8008 -u 0x12343bdgf.worker
- **beepool:** nbminer -a ethash -o ethproxy+tcp://eth-pool.beepool.org:9530 -u 0x12343bdgf.worker
- **nanopool:** nbminer -a ethash -o ethproxy+tcp://eth-asia1.nanopool.org:9999 -u 0x12343bdgf.worker
- **herominers:** nbminer -a ethash -o ethproxy+tcp://ethereum.herominers.com:10201 -u 0x12343bdgf.worker
- **nicehash:** nbminer -a ethash -o nicehash+tcp://daggerhashimoto.eu.nicehash.com:3353 -u btc_address.worker

#### BTM+ETH

- **f2pool:** nbminer -a tensority_ethash -o stratum+tcp://btm.f2pool.com:9221 -u btm_address.btm_worker -do ethproxy+tcp://eth.f2pool.com:8008 -du eth_address.eth_worker


#### SERO

- **beepool**: nbminer -a progpow_sero -o stratum+tcp://sero-pool.beepool.org:9515 -u wallet_address.worker:pswd
- **f2pool**: nbminer -a progpow_sero -o stratum+tcp//sero.f2pool.com:4200 -u wallet_address.worker:pswd


#### BFC

- **uupool**: nbminer -a bfc -o stratum+tcp://bfc.uupool.cn:12210 -u username.worker
- **bfcpool**: nbminer -a bfc -o stratum+tcp://ss.bfcpool.com:3333 -u wallet.worker

#### HNS

- **f2pool**: nbminer -a hns -o stratum+tcp://hns.f2pool.com:6000 -u wallet.worker
- **6block**: nbminer -a hns -o stratum+tcp://handshake.6block.com:7701 -u username.worker

#### HNS+ETH:

- **f2pool**: nbminer -a hns_ethash -o stratum+tcp://hns.f2pool.com:6000 -u wallet.worker -do stratum+tcp://eth.f2pool.com:8008 -du wallet.worker


## CMD options：

**nbminer -a algo -o protocol+socket_type://pool_host:pool_port -u wallet_address.worker:passwd**

  * -h, --help    Displays this help.
  * -v, --version    Displays version information.
  * -c, --config \<config file path>    Use json format config file rather than cmd line options.
  * -a, --algo \<algo>    Select mining algorithm
  * --api  \<host:port>    The endpoint for serving REST API.
  * -o, --url \<url>    Mining pool url.
  * -u, --user \<user>    User used in Mining pool, wallet address or username.
      * Format: [username|wallet].workername:password
  * -o1, --url1 \<url> url for backup mining pool 1.
  * -u1, --user1 \<user> username for backup mining pool 1.
  * -o2, --url2 \<url> url for backup mining pool 2.
* -u2, --user2 \<user> username for backup mining pool 2.
* -di, --secondary-intensity \<intensity>    The relative intensity when dual mining.
* -do, --secondary-url \<url>    ETH mining pool when dual mining.
* -du, --secondary-user \<user>    ETH username when dual mining.
* -do1, --secondary-url1 \<url>    Backup 1 ETH mining pool when dual mining.
* -du1, --secondary-user1 \<user>    Backup 1 ETH username when dual mining.
* -do2, --secondary-url2 \<url>    Backup 2 ETH mining pool when dual mining.
* -du2, --secondary-user2 \<user>    Backup 2 ETH username when dual mining.
* -d, --devices \<devices>    Specify GPU list to use. Format: "-d 0,1,2,3" to use first 4 GPU.
* -i, --intensity \<intensities>    Comma-separated list of intensities (1 -100).
* --strict-ssl    Check validity of certificate when use SSL connection.
* --proxy    Socks5 proxy used to eastablish connection with pool, E.g. 127.0.0.1:1080
* --cuckoo-intensity \<intensity>    Set intensity of cuckoo, cuckaroo, cuckatoo, [1, 12]. Smaller value means higher CPU usage to gain more hashrate. Set to 0 means autumatically adapt. Default: 0.
* --cuckatoo-power-optimize    Set this option to reduce the range of power consumed by rig when minining with algo cuckatoo. This feature can reduce the chance of power supply shutdown caused by overpowered. Warning: Setting this option may cause drop on minining performance.
* --temperature-limit \<temp-limit>    Set temperature limit of GPU, if exceeds, stop GPU for 10 seconds and continue.
* --log    Generate log file named `logs/log_<timestamp>.txt`.
* --log-file \<filename>    Generate custom log file. Note: This option will override `--log`.
* --no-nvml    Do not query cuda device health status.
* --fidelity-timeframe \<timeframe>    Set timeframe for the calculation of fidelity, unit in hour. Default: 24.
* --long-format    Use 'yyyy-MM-dd HH:mm:ss,zzz' for log time format.
* --verbose    Print communication data between miner and pool in log file.
* --device-info    Print device cuda information.
* --fee \<fee>    Change devfee in percentage, [0-5]. Set to '0' to turn off devfee with lower hashrate. Otherwise, devfee = max(set_value, def_value).
* --generate-config \<filename>    Generate a sample config json file.
* --no-watchdog    Disable watchdog process.
* --platform \<platform>    Choose platform，0: NVIDIA+AMD (default), 1: NVIDIA only, 2: AMD only
* --coin \<coin>    Set coin for ethash algo. E.g, eth, etc
* --share-check \<value>    If \<value> minutes without share, reboot miner, set 0 to disable. Default: 30
* --no-interrupt    set this option will disable miner interrupting current GPU jobs when a new job coming from pool, will cause less power supply issue, but might lead to a bit higher stale ratio and reject shares.
* **--mt, --memory-tweak \<mode>    Memory timings optimize for Nvidia GDDR5 & GDDR5X gpus. range [1-6]. Higher value equals higher hashrate. Individual value can be set via comma seperated list. Power limit may need to be tuned up to get more hashrate. Higher reject share ratio can happen if mining rig hits high temperature, set lower value of `-mt` can reduce reject ratio. Under windows, a custom driver need to be installed when using `-mt`, can installed manually by option  `--driver`, or run nbminer.exe with admin privilege to perform auto-install. Under linux, admin priviledge is needed to run, `sudo ./nbminer -mt x`. `OhGodAnETHlargementPill` is not needed anymore if `-mt` is enabled when mining on 1080 & 1080ti GPUs.**
* **--driver \<action>    Windows only option, install / uninstall driver for `memory tweak`. Run with admin priviledge. install: `nbminer.exe --driver install`, uninstall: `nbminer.exe --driver uninstall`. **


### Response

``` json
{
    "miner": {
        "devices": [
            {
                "accepted_shares": 2,
                "accepted_shares2": 0,
                "core_clock": 1620,
                "core_utilization": 100,
                "fan": 47,
                "fidelity1": 5.859799716605649,
                "fidelity2": 0,
                "hashrate": "217.1 M",
                "hashrate2": "36.19 M",
                "hashrate2_raw": 36190716.266428046,
                "hashrate_raw": 217144297.59856823,
                "id": 0,
                "info": "GeForce RTX 2070",
                "mem_clock": 6801,
                "mem_utilization": 86,
                "pci_bus_id": 1,
                "power": 188,
                "rejected_shares": 0,
                "rejected_shares2": 0,
                "temperature": 72
            },
            {
                "accepted_shares": 0,
                "accepted_shares2": 0,
                "core_clock": 1607,
                "core_utilization": 100,
                "fan": 0,
                "fidelity1": 0,
                "fidelity2": 0,
                "hashrate": "168.5 M",
                "hashrate2": "42.11 M",
                "hashrate2_raw": 42113955.19774488,
                "hashrate_raw": 168455820.79097953,
                "id": 1,
                "info": "P102-100",
                "mem_clock": 5508,
                "mem_utilization": 100,
                "pci_bus_id": 4,
                "power": 232,
                "rejected_shares": 0,
                "rejected_shares2": 0,
                "temperature": 57
            }
        ],
        "total_hashrate": "708 M",
        "total_hashrate2": "164.4 M",
        "total_hashrate2_raw": 164395439.13815895,
        "total_hashrate_raw": 708044466.8349969,
        "total_power_consume": 839
    },
    "reboot_times": 0,
    "start_time": 1586944619,
    "stratum": {
        "accepted_shares": 2,
        "accepted_shares2": 0,
        "algorithm": "hns_ethash",
        "difficulty": "8.59 G",
        "difficulty2": "8.59 G",
        "dual_mine": true,
        "latency": 221,
        "latency2": 0,
        "rejected_shares": 0,
        "rejected_shares2": 0,
        "url": "handshake.hk.nicehash.com:3384",
        "url2": "daggerhashimoto.hk.nicehash.com:3353",
        "use_ssl": false,
        "use_ssl2": false,
        "user": "3QHNv52ahdCyeYTGVYDPGjRzMpkknjjfAf.test",
        "user2": "3QHNv52ahdCyeYTGVYDPGjRzMpkknjjfAf.test"
    },
    "version": "30.0"
}
```

## Change Log

#### v0.1.1

- Improve HNS & HNS+ETH on Nvidia GPU
