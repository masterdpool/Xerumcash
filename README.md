# Xerumcash Coin
Shell script to install a [Xerumcash Masternode](http://www.xerumcash.com/) on a Linux server running Ubuntu 16.04. Use it on your own risk.
***

## VPS installation
```
wget -q https://raw.githubusercontent.com/Realbityoda/Xerumcash/master/xerumcash_install.sh
bash xerumcash_install.sh
```
***

## Desktop wallet setup  

After the MN is up and running, you need to configure the desktop wallet accordingly. Here are the steps:  
1. Open the Xerumcash Desktop Wallet.  
2. Go to RECEIVE and create a New Address: **MN1**  
3. Send **1000** Xerumcash to MN1. You need to send all **1000** coins in one single transaction.
4. Wait for 15 confirmations.  
5. Go to **Help** -> "**Debug Window** - Console"  
6. Type the following command: **masternode outputs**  
7. Go to  **Tools** -> "Open Masternode Configuration File"**
8. Add the following entry:
```
Alias Address Privkey TxHash TxIndex
```
* Alias: **MN**
* Address: **VPS_IP:PORT**
* Privkey: **Masternode Private Key**
* TxHash: First value from Step 6
* TxIndex:  Second value from Step 6
9. Save and close the file.
10. Go to Masternode Tab. If you tab is not shown, please enable it from: Settings - Options - Wallet - Show Masternodes Tab
11. Click Update status to see your node. If it is not shown, close the wallet and start it again. Make sure the wallet is un
12. Select your MN and click Start Alias to start it.
13. Alternatively, open Debug Console and type:
```
startmasternode "alias" "0" "MN1"
``` 
14. Login to your VPS and check your masternode status by running the following command:.
```
XerumCash-cli masternode status
```


## Usage:
```
XerumCash-cli masternode status  
XerumCash-cli getinfo
```
Also, if you want to check/start/stop **XerumCash**, run one of the following commands as root:

```
systemctl status XerumCash #To check if XerumCash service is running  
systemctl start XerumCash #To start XerumCash service  
systemctl stop XerumCash #To stop XerumCash service  
systemctl is-enabled XerumCash #To check if XerumCash service is enabled on boot  
```  


## Donations

Any donation is highly appreciated

**XerumCash**: yCkkGmyWTHTzkbEqqiNb7pt9W1ez7n25XF  
**BCH**: qzgnck23pwfag8ucz2f0vf0j5skshtuql5hmwwjhds  
**ETH**: 0x765eA1753A1eB7b12500499405e811f4d5164554  
**LTC**: LNt9EQputZK8djTSZyR3jE72o7NXNrb4aB  
