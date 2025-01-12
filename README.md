# Grin Wallet Tutorial

This tutorial will teach you how to create [command line wallet with grin-wallet](#command-line-grin-wallet) and [gui wallet with grim](#grim-gui-wallet).

## Command line grin wallet

1. Download the wallet: [https://github.com/mimblewimble/grin-wallet/releases](https://github.com/mimblewimble/grin-wallet/releases).

2. Create new wallet: `./grin-wallet init -h`.
Ignore the errors and set the password, the command will create the wallet in the current directory.
![image](https://github.com/user-attachments/assets/5de41b6e-f8ed-437d-b482-215da0dd30db)
> [!NOTE]
> If you need to recreate your wallet from an existing seed, use `./grin-wallet init -hr` command.

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

## Grim GUI wallet

1. Download the wallet: [https://gri.mw/#downloads](https://gri.mw/#downloads)

2. Create a wallet by clicking on `ADD WALLET` button and set wallet name and password:
![image](https://github.com/user-attachments/assets/6203347b-7ace-4dfc-98df-e4a55e0baab9)
![image](https://github.com/user-attachments/assets/5ee085be-8513-4ade-8607-a65c51e9ff94)

3. Write down your seed and press on `CONTINUE` button:
![image](https://github.com/user-attachments/assets/a49a5868-fb00-4e55-a911-70e352fc436f)
> [!NOTE]
> If you need to recreate your wallet from an existing seed, choose `Restore` checkbox.

4. On the next step, the app will ask you to input your seed to verify the correctness. Input it and press `CONTINUE`.

5. The final step is to choose the connection method. It could be your local node (integrated) or public node (external). Here we'll choose external connection for quick wallet synchronization. Click on the checkmark near `https://grincoin.org` and press `COMPLETE` button.

![image](https://github.com/user-attachments/assets/79468598-c452-43af-bb1a-1fe5d0b2ddb4)

6. Now wait for wallet synchronizaion completion. It could take several minutes.



