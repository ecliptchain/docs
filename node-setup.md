
# **Tutorial - Install Eclipt Node on Ubuntu Server 22.04**

Follow this tutorial to install a node for your **Eclipt** coin on **Ubuntu Server 22.04**.

## **1. Update Your Server**
Run the following command to update and upgrade your Ubuntu server:
```bash
sudo apt-get update && sudo apt-get upgrade -y
```

## **2. Download the Linux Daemon**
Use the following command to download the **Eclipt daemon**:
```bash
wget "https://github.com/ecliptchain/docs/releases/download/eclipt-daemon-linux/eclipt-daemon-linux.tar.gz" -O eclipt-daemon-linux.tar.gz
```

## **3. Extract the Daemon Files**
Run this command to extract the downloaded `.tar.gz` file:
```bash
tar -xzvf eclipt-daemon-linux.tar.gz
```

## **4. Download the Linux Tools**
Use the following command to download the **Eclipt wallet tools**:
```bash
wget "https://github.com/ecliptchain/docs/releases/download/eclipt-daemon-linux/eclipt-daemon-linux.tar.gz" -O eclipt-qt-linux.tar.gz
```

## **5. Extract the Tools**
Extract the `.tar.gz` file using:
```bash
tar -xzvf eclipt-qt-linux.tar.gz
```

## **6. Install the Daemon and Tools**
Move the daemon and tools to `/usr/bin/` so they can be used system-wide:
```bash
sudo mv ecliptd eclipt-cli eclipt-tx /usr/bin/
```

## **7. Create the Data Directory**
Run this command to create a directory for Eclipt data:
```bash
mkdir $HOME/.eclipt
```

## **8. Configure the Node**
Open the configuration file using `nano`:
```bash
nano $HOME/.eclipt/eclipt.conf -t
```
Paste the following configuration into `nano`:
```ini
rpcuser=rpc_user
rpcpassword=rpcpassword
rpcbind=127.0.0.1
rpcallowip=127.0.0.1
listen=1
server=1
txindex=1
daemon=1
```
Save and exit **nano** using:  
Press `CTRL + X`, then `Y`, and press `Enter`.

## **9. Start Your Node**
Run the following command to start your Eclipt node:
```bash
ecliptd
```

### 🎉 **Your Eclipt node is now running!** 🎉  
You can check the node status using:
```bash
eclipt-cli getinfo
```

