### 📌 **Guide to Staking Eclipt (ECL)**  

Eclipt is a cryptocurrency that works on the Proof-of-Work (POW) algorithm and also Proof-of-Stake (PoS). This means that instead of mining, new coins are used to store their account in the wallet and participate in the network.

---

## 🔹 **1. Installing the Eclipt Wallet**  
### 🖥 For Windows/Linux/macOS  
1. Download the official **Eclipt Core** wallet from [the official website or project repository].  
2. Install and launch the wallet. Wait for the blockchain to sync.  

---

## 🔹 **2. Configuring the Wallet for Staking**  
### 📂 Locate the Configuration File  
The `eclipt.conf` file is located at:  
- **Windows**: `C:\Users\YourUser\AppData\Roaming\Eclipt\eclipt.conf`  
- **Linux**: `~/.eclipt/eclipt.conf`  
- **macOS**: `~/Library/Application Support/Eclipt/eclipt.conf`  

If the file does not exist, create it. Open it in a text editor and add the following lines:  
```ini
server=1
daemon=1
staking=1
rpcuser=Your_Username
rpcpassword=Your_Password
```
Save and close the file.

---

## 🔹 **3. Unlocking the Wallet for Staking**  
If your wallet is **encrypted**, run the following command in the console:  
```
walletpassphrase "YOUR_PASSWORD" 9999999 true
```  
- `9999999` — unlock duration (in seconds).  
- `true` — enables **staking only** (without allowing fund transfers).  

**Check staking status:**  
```
getstakinginfo
```
If `staking: true`, staking is active.

---

## 🔹 **4. Tips to Increase Rewards**  
✅ **Keep your wallet online 24/7** — the longer it runs, the higher the chance of receiving rewards.  
✅ **The more coins you hold, the higher your staking rewards.**  
✅ **Wait for "coin age"** — coins start participating in staking **8 hours** after being received.  

---

## 🔹 **5. Disabling Staking**  
If you want to **disable staking**, run the following command:  
```
walletpassphrase "YOUR_PASSWORD" 9999999 false
```  
Then check the status:  
```
getstakinginfo
```
If `staking: false`, staking is disabled.

---

💡 **Done! Your Eclipt wallet is now generating passive income through staking.** 🚀
