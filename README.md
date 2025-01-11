# Grin Wallet Tutorial

This tutorial will teach you how to create Grin command line wallet as easy as possible.

1. Download the wallet: [https://github.com/mimblewimble/grin-wallet/releases](https://github.com/mimblewimble/grin-wallet/releases).

2. Create new wallet: `./grin-wallet init -h`.
Ignore the errors and set the password, the command will create the wallet in the current directory.
![image](https://github.com/user-attachments/assets/5de41b6e-f8ed-437d-b482-215da0dd30db)

3. Find `grin-wallet.toml` file in the current directory and edit it as follows:
![image](https://github.com/user-attachments/assets/596b6782-5bc2-48c3-b45b-9d99af4950a4)
As you can see, we commented `api_secret_path`, `node_api_secret_path` and added `https://grincoin.org` public node. You can also use `https://grinnode.live:3413` node.

4. Run `./grin-wallet info` command and wait for the wallet scanning completion, this could take several minutes.
![image](https://github.com/user-attachments/assets/b20479d2-65ff-44ac-9bf4-6aa978db6d9b)

That's it. The wallet is fully set and ready to make your first transaction.

5. Receive.
* Run `./grin-wallet receive` and paste Satepack message that you should get from sender:
![image](https://github.com/user-attachments/assets/39a46302-7674-44af-886e-a0a04f67b65d)
The command will return a Slatepack which you should provide to the sender.

6. Send.
* Run `./grin-wallet send 1` (sending 1 coin), copy the returned Slatepack message and provide it to receiver.
* Get Slatepack message from the receiver, run `./grin-wallet finalize` command and copy-paste the Slatepack into it.

For the complete guide go to: [https://docs.grin.mw/getting-started/wallet-handbook/](https://docs.grin.mw/getting-started/wallet-handbook/)
