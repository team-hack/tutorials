# Getting Started with Detonus

Hey everyone, we get a lot of questions about [DETONUS](https://detonus.com/). I thought I'd make a resource that will cover the basics. Detonus is basically a fork of Ethereum with some adjustments to the Ethash, to provide GPU and ASIC mining resistance. With that being said, it is one of the most appealing CPU mineable projects at the moment. 

### Downloading Wallet
Detonus currently uses the Goland Implementation of the Blockchain which is command based standalone client software. The wallet client can be downloaded from the [Detonus v1.1.2-stable release.](https://github.com/detonus-project/go-detonus/releases/tag/v1.1.2-stable)
Once you've downloaded the appropriate client software to your OS, unzip/untar the archive to your desired location.

### Running the Wallet

You now need to run your Terminal/Command Prompt.
- Mac: Click the Launchpad icon  in the Dock, type Terminal in the search field, then click Terminal.
- Linux: You can open Terminal by directly pressing ```ctrl+alt+T```
- Windows: Press the ```Windows Key+S``` to start the search console in Windows and type ```CMD``` Select and start CMD.exe

Once you've started your Terminal/Command Prompt you'll need to navigate to the appropriate folder where your client software is stored to be able to run it.
Let's assume that you've extracted the Wallet Client Software to your Desktop, you'll need to navigate to your Desktop by using the change directory command:
```cd /home/yourlinuxuser/Desktop/``` or ```cd Desktop```
Now you are ready to connect to the Client Software.

Let's start by Creating an Account. To do so, copy/paste the command below that is applicable to your OS. Pasting in your Terminal/Command Prompt is done by right clicking on your Terminal/Command Prompt and not with ```ctrl+V```
**Windows:** ```geth_windows_amd64.exe --datadir ./.detonus account new```
**Linux:** ```./geth_linux_amd64 --datadir ./.detonus account new```
**Macos:** ```./geth_darwin_amd64 --datadir ./.detonus account new```
After that please create a password that you will use to unlock your account. Type that into the Terminal/Command Prompt and confirm it when prompted to repeat it again.
You will receive this confimation message appearing in your Terminal/Command Prompt.
```Your new key was generated```
You will see your Public address, in my case it is```0x596FBEB926a98eC1ebCD0e2f554EFDe909E696D7```
And you'll get the path of the secret key file which you can back up for safe keeping ```.detonus\keystore\UTC--2021-10-06.....```
You will also get this valuable info:
- You can share your public address with anyone. Others need it to interact with you.
- You must NEVER share the secret key with anyone! The key controls access to your funds!
- You must BACKUP your key file! Without the key, it's impossible to access account funds!
- You must REMEMBER your password! Without the password, it's impossible to decrypt the key!

### Connecting to the Detonus network
Start your wallet by running the command in applicable to your OS.
**Windows:** ```geth_windows_amd64.exe --datadir ./.detonus --unlock "YOUR_ADDRESS" console```
**Linux:** ```./geth_linux_amd64 --datadir ./.detonus --unlock "YOUR_ADDRESS" console```
**Macos:** ```./geth_darwin_amd64 --datadir ./.detonus --unlock "YOUR_ADDRESS" console```
Between the brackets where it says YOUR_ADDRESS, input your public address, which in my case it is ```0x596FBEB926a98eC1ebCD0e2f554EFDe909E696D7```
Now enter the password you created earlier.

Your wallet will now start looking for peers to sync with the blockchain. In case it fails to connect to the peers by itself, please use one of the 2 methods below to add static peers to your wallet.
**Temporary:** ```admin.addPeer("")```
**Permanent:** ```--discovery.dns ""```
You will now need to enter the peer IDs between the brackets **""** on either one of those methods.
- Peer list that I am currently using:
```enode://cb5431669114e9797ddc4d17c1da64e9806f92030868e6d1c14b4467c94073b3fe84909071c633cac179b09c8dabdd484704fbd20755369c5435d7396fa2a33f@65.21.193.162:30303```
```enode://d834762aa2569d238a882f6066df93e1d6ea362b21baa1ba98303d68ea91b824fc91c8a3b00e803144318c09e2562aedd2809fed4cb30dc3acff3ceccf7803de@194.156.98.125:30303```
```enode://bae927dedfdf38206edf00a8527578e24913d55192da780272fb2b02fffb60181bd9262f7445a7c661fa2c11255a7e169cd64bab088b06ca086d0d2dc5be9737@185.87.151.155:30303```
```enode://f09a29f37c00301a40816de4367e214620a35ac7ba3061427c6be8d8009dc22b4dba382600f893953a2484e991f1db1be1cc38c16ebde23474d8c11ff52337cc@195.204.173.78:30303```
```enode://296b13b57c0b3efea09fefbd8b72161bfdbefda1447b70834defcd78f8507d51a61bf9298959236b9d8bd416d6930633d39fa87c397f7d682cf151fd9be4b75c@79.102.158.193:30303```
```enode://f963f735ee158a9e038ea9867be0492d8d490c9bf5fa02c412359ec3bb39286dcc2ba80b45b0276d70cfd067acce46d69c2c776fc40ba9f19afa3227d3c2fffe@2.29.85.92:30303```
```enode://d4c10b5920842154116ea665c68bbcdbcc0befd679c43ed669310af1dc46ab0fc3d4b661634c525bf19b852d336c80346f517a47329a9cfd123fbfc2abdbb4fb@95.84.245.85:30303```

Adding a temporary peer command should look like this:
```admin.addPeer("enode://cb5431669114e9797ddc4d17c1da64e9806f92030868e6d1c14b4467c94073b3fe84909071c633cac179b09c8dabdd484704fbd20755369c5435d7396fa2a33f@65.21.193.162:30303")```
After a few attempts, your wallet will start syncing with the network.

### Mining from your Wallet
To start mining in a new Terminal/Command Prompt window, start a new terminal session and paste the command applicable to your OS.

**Windows:** ```geth_windows_amd64.exe --datadir ./.detonus --mine --miner.threads 64 --miner.etherbase "YOUR_ADDRESS" console```
**Linux:** ```./geth_linux_amd64 --datadir ./.detonus --mine --miner.threads 64 --miner.etherbase "YOUR_ADDRESS" console```
**Macos:** ```./geth_darwin_amd64 --datadir ./.detonus --mine --miner.threads 64 --miner.etherbase "YOUR_ADDRESS" console```
Between the brackets where it says YOUR_ADDRESS, input your public address, which in my case it is ```0x596FBEB926a98eC1ebCD0e2f554EFDe909E696D7```
At the point of the command ```--miner.threads 64``` please enter the number of CPU threads that your CPU has, and you're willing to dedicate to mining Detonus.

Here is an example what the command should look like:
```geth_windows_amd64.exe --datadir ./.detonus --mine --miner.threads 2 --miner.etherbase "0x596FBEB926a98eC1ebCD0e2f554EFDe909E696D7" console```
This command instructs my PC to mine Detonus with 2 threads and the rewards for any minted blocks will be sent to my 0x596FBEB926a98eC1ebCD0e2f554EFDe909E696D7 address.

To start mining on top of your previous session just paste the command:
```--mine --miner.threads (number.of.threads)``` or to mine Detonus with 2 threads paste ```--mine --miner.threads 2```

To check you mining power/hashrate please use this command:
```web3.eth.hashrate```

### Check Your Balance from your Wallet

To check your account balance from the wallet, make sure that you're wallet is unlocked and you are running the geth console. If you followed the steps above you're fine. If you are starting a new Terminal/Command Prompt session please use the command below applicable to your OS:
**Windows:** ```geth_windows_amd64.exe --datadir ./.detonus --unlock "YOUR_ADDRESS" console```
**Linux:** ```./geth_linux_amd64 --datadir ./.detonus --unlock "YOUR_ADDRESS" console```
**Macos:** ```./geth_darwin_amd64 --datadir ./.detonus --unlock "YOUR_ADDRESS" console```
Between the brackets where it says YOUR_ADDRESS, input your public address. In my case it is ```0x596FBEB926a98eC1ebCD0e2f554EFDe909E696D7```
Your final command should look like this ```geth_windows_amd64.exe --datadir ./.detonus --unlock "0x596FBEB926a98eC1ebCD0e2f554EFDe909E696D7" console```
Now enter the password that unlocks your account.

Now enter this command in the console:
```web3.fromWei(eth.getBalance("YOUR_ADDRESS"), "ether")```
Between the brackets where it says YOUR_ADDRESS, input your public address. In my case it is ```0x596FBEB926a98eC1ebCD0e2f554EFDe909E696D7```
Your final command should look like this: ```web3.fromWei(eth.getBalance("0x596FBEB926a98eC1ebCD0e2f554EFDe909E696D7"), "ether")```
This will print display the current Detonus balance on your account.

### Sending Transactions
To send a transaction to someone, you will need to have a balance that is >0 and you will need to know their public address.
To send DT you can use the command ```eth.sendTransaction({from: "YOUR_ADDRESS",to: "RECEIVER_ADDRESS", value: ""})```
Between the brackets where it says YOUR_ADDRESS, input your public address. Between the brackets where it says RECEIVER_ADDRESS, input your receiver's public address. Between the brackets after value: enter the ammount of Detonus that you want to send to the receiver.

In a test, we sent a value of 1000000 to determine how much DT it will transact.
```eth.sendTransaction({from: "0x542e54933509b7a617a5e85baceeb42dae22986e",to: "0xd598d864d87264c6686de16155f14574aefe5d90", value: "1000000"})```
The sender ```0x542e54933509b7a617a5e85baceeb42dae22986e``` sent to ```0xd598d864d87264c6686de16155f14574aefe5d90``` a total of 0.01 DT.

[Here is the transaction on the Explorer.](https://explorer.detonus.com/tx/0x68fe23b89dceeaea0a1ae9f58d84a2c5c9f6c9489a779e76d7c9cabc6e53a973)
To calculate values of transaction you need to know the number of denominations of Detonus. Detonus has **8** .00000000 decimal points. That is why the value of 1 million got ended up being displayed as a 0.01 DT transaction.  

If you found this beginners' guide to Detonus, you can share it with a friend who might benefit from it and/or support me by donating some Detonus to ```0x596FBEB926a98eC1ebCD0e2f554EFDe909E696D7```
