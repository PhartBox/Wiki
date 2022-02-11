### Easy and step by step fast guide for mining on non-rooted Android mobile phones (Termux with CCminer or VerusMiner9000)

### Ingredients you need for mining:
* Wallet -> [GET IT HERE](https://verus.io/wallet)
* Android mobile phone or other Android device (this guide focuses on mobile phone but same procedure can work on tablets and even on android tv box and similar)
* Pool where you are going to mine -> [SELECT ONE HERE](https://miningpoolstats.stream/veruscoin)  
<details><summary>CLICK TO READ BASIC INFO HOW TO SELECT POOL </summary>
<p>
We recommend official pool from verus.io . This pool has a 5% fee, which is intended to be higher than other pools. Any and all proceeds go directly to the Verus Foundation and are used at its discretion for community bounties, listing drives, and other expenses, with the sole purpose of realizing the Verus Vision.<br>
When you decide which pool you like depending on fees and location proceed and select it. You should be redirected to official pool webpage where you have to search for pool address. It should look like this: pool.verus.io:19999 . You are going to need this address with your wallet address later for mining software.
</p>
</details>

### Android device must have:
* 64-bit processor with AES functions enabled
* 64-bit operating system
* Free space: from 1GB - 3.5 GB+
* Android 7.0 ->
* It is recommended that your device is properly cooled. Mining can make your device overheat and there is potential fire hazard or battery explosion. Mine at your own risk!

Generally speaking the easiest way to know if your Android device is running 64-bit OS is if device has 4GB RAM or more. If it shows less then you will have to double check. Easiest method is by checking kernel version. To do that I suggest to install CPU-Z app(or something similar) and check under System tab on Kernel Architecture indication for 64-bit. Next step would be to make sure CPU is ARM capable. For this I also suggest to use CPU-Z under SOC tab there should be ARM indication on Architecture for CPU in device.
#### If you are planning to buy used or damaged Android device just for mining purpose i suggest to search for device on https://www.devicespecifications.com/ or some similar site where you can find information about OS and CPU to meet 64-bit requirements, available space and Android version.

### If all conditions are met then you can continue further on selecting your mining software below and start mining

<details><summary> EASY WAY CLICK TO READ </summary>
<p>

#### VerusMiner9000
1. Download&Install Verus Miner 9000 from: https://github.com/shmutalov/VerusMiner9000/releases
2. Open it & Enter or create your wallet.
3. Select mining pool. We recommend Verus Project pool
4. Select hardware settings. We recommend testing different settings.
5. Press I am ready button & earn VRSC
</p>
</details>

<details><summary>ADVANCED CLICK TO READ </summary>

##### You can choose between multiple mining solutions. Here are two versions. First one is a bit shorter and both produce pretty much same results but it is up for miner to decide.

#### Termux + CCminer1010
1. Download&Install Termux - recommend 0.117 and above version from: https://f-droid.org/en/packages/com.termux/
2. Open Termux app
3. Enter commands in following order and wait for each to finish doing whatever it's doing & don't panic:
* apt update && apt upgrade -y
* pkg install git
* pkg install cmake
* pkg install proot
* pkg install proot-distro
* proot-distro install ubuntu
* proot-distro login ubuntu
* apt-get update && apt-get upgrade -y
* apt-get install libcurl4-openssl-dev libssl-dev libjansson-dev automake autotools-dev build-essential git nano
* git clone --single-branch -b ARM https://github.com/monkins1010/ccminer
cd ccminer
* chmod +x build.sh && chmod +x configure.sh && chmod +x autogen.sh
* ./build.sh
* (depending on your location and pool, change wallet address and worker name and last number 8 represents number of cores you want to use. Depends on your devices core count!!! If device is overheating or heats too much lover that number!) use last command: ./ccminer -a verus -o stratum+tcp://eu.luckpool.net:3956 -u WALLETADDRESS.PHONENAME -p d=4096S -t 8


#### Termux + CCminer rk3328
1. Download&Install Termux - recommend 0.117 and above version from: https://f-droid.org/en/packages/com.termux/
2. Open Termux app
3. Enter commands in following order and wait for each to finish doing whatever it's doing & don't panic:
* apt update && apt upgrade -y
* pkg install git
* pkg install cmake
* pkg install proot
* pkg install proot-distro
* pkg upgrade
* pkg install root-repo
* proot-distro install ubuntu
* proot-distro login ubuntu
* apt-get update && apt-get upgrade -y
* apt-get install libcurl4-openssl-dev libssl-dev libjansson-dev automake autotools-dev build-essential git nano
* pkg install clang
* git clone https://github.com/DevTechGames/ccminer-rk3328.git
* cd ccminer-rk3328
* chmod +x build.sh && chmod +x configure.sh && chmod +x autogen.sh
* pico configure.sh
* modify clang version from 10 -> 13 by using arrow keys on the termux keyboard. Go to bottom line and press END then use back arrow key until you find clang version 10 and change it to 13. Then press CONTROL then X to exit confirm changes with Y and then Enter.
* ./build.sh
* (depending on your location and pool, change wallet address and worker name and last number 8 represents number of cores you want to use. Depends on your devices core count!!! If device is overheating or heats too much lover that number!) use last command: ./ccminer -a verus -o stratum+tcp://eu.luckpool.net:3956 -u WALLETADDRESS.PHONENAME -p d=4096S -t 8
</details>

#### Welcome to Verus mining family!
