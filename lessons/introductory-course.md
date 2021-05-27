TODO How to send a transaction

# Basic Tutorial Layout

## :fox_face: Setting up a MetaMask Wallet

*What is a wallet?*

You can think of a wallet as a door to access cryptocurrencies you own. Only you have the private key, consisting of 64 alphanumerical characters. If anyone else knows your private key, they can access and transfer your cryptocurrencies. 

`e.g. 7de100578f780be29f9adb841026985824e9a7f948a2877c31e0d9cca756a080`

A private key is generated from a 12 word seed phrase unique to your wallet. Because anyone who knows your seed phrase can generate your private key, they can also access and transfer your cryptocurrencies. 

`e.g. black enough endless person bone term worry plastic detect distance sting employ`

It is important to remember that a wallet is only a tool to access and transfer your cryptocurrencies. If you accidentally uninstall your wallet extension or app, a record of your account still exists on the blockchain. As long as you remember you private key or seed phrase, you will be able to access your crypto again.

*What is a blockchain?*

A blockchain is a collection of devices that are connected to each other through the internet. It is different from the internet because its main function is to keep track of quantifiable value in the form of cryptocurrencies like Ethereum or Bitcoin. Each device on the blockchain called a node. Nodes constantly communicate with each other, verifying that other nodes contain a truthful depiction of the balances of accounts on the blockchain.  

You will now create your first wallet using MetaMask. [Click here to install MetaMask and follow the instructions in the app](https://metamask.io/download.html). Remember to keep your seed phrase somewhere safe!

---

## :satellite: How to switch Metamask to the xDai network

By default, MetaMask is connected to the Ethereum network. You can verify this by looking at the top right of your MetaMask extension. Ether is the native currency of the Ethereum network and Ether account balances are constantly verified using blockchain technology. 

There are also other networks that are built to complement the Ethereum network. One of these networks is the xDai chain, which allows for fast and inexpensive transactions. It also has its own native currency, xDai. To learn about the blockchain in a relatively low-risk environment, we will be using the xDai chain. Feel free to explore other networks after this lesson.  

To connect to the xDai chain, we need to add it as a custom network. You can [follow the instructions on the official website here](https://www.xdaichain.com/for-users/wallets/metamask/metamask-setup). It is always recommended that you only add custom networks by following instructions from official documentation. Your network details should look something like this:  

<img alt="xdai rpc settings" src="https://user-images.githubusercontent.com/83733789/118858811-c5ea3d80-b896-11eb-95a7-2a9c07c631b9.png" width=25%>

If you are on mobile, you can add a custom network by tapping **Networks** in **settings**.

---

## :money_with_wings: How to get xDai

To interact with the blockchain, we need cryptocurrency. There are two main ways to get xDai: exchange fiat(government-backed currency) for crypto or through the xDai faucet. For our purposes, we will be using a faucet to receive xDai. 

*What is a faucet?*

A faucet is a place where you can request cryptocurrency to be sent to your address. Nowadays, there aren't many active faucets anymore.

>Fun fact: Bitcoin once had a faucet that gave five bitcoins per person. 

*What is an address?*

Remember your private key? Using the private key, an individual can also generate a public key that is simplified into a 42 character long address. If someone knows your address, they can view how much cryptocurrency you have in your account and send you crypto.  

It is safe to share your address because a private key can be used to generate a public key but a public key cannot be used to generate a private key.  

We will now use the faucet to send some xDai to our own address. Follow the [instructions on the official website to receive xDai in your wallet](https://www.xdaichain.com/for-users/get-xdai-tokens/xdai-faucet). You can copy your wallet address by tapping on it.

<img alt="wallet address" src="https://user-images.githubusercontent.com/83733789/118893916-7882c600-b8c0-11eb-90fa-c6eebf33f516.png" width=25%>


After you have requested xDai from a faucet, click **View in Explorer** to open the xDai blockchain explorer Blockscout.

<img alt="view wallet transactions on blockscout" src="https://user-images.githubusercontent.com/83733789/119557697-be76d880-bd5d-11eb-80d6-bfd1eba54633.png" width=25%>

*What is a blockchain explorer?*

Every transaction on a blockchain is recorded in groups, called blocks. Blockchain explorers allow its users to view the details of every transaction ever made on the blockchain. You can also view the all transactions of a specific addresses as well.  

For now, we will be using the block explorer to look for an incoming transaction from an xDai faucet. When you see that a successful transaction has been made, move on to the next section.  

<img alt="blockscout view" src="https://user-images.githubusercontent.com/83733789/119561500-7dcd8e00-bd62-11eb-97c0-46fe1ccdddf5.png" width=75%>

---

## :mag: Using the blockchain explorer

Every transaction on the blockchain requires a certain fee to complete. In the Ethereum and xDai ecosystem, this fee is referred to as gas. Gas price is measured in gigawei(or gwei) and is one billionth of an Ether or xDai.  

Click on the transaction hash of the incoming transaction from an xDai faucet, beside the **transfer** label. 

<img alt="blockscout transaction" src="https://user-images.githubusercontent.com/83733789/119698794-d78b9200-be0e-11eb-9d28-30dab91048fc.png" width=75%>

Here you can see all the details of your transaction. Transactions on the blockchain are grouped into blocks and processed together. You can see all the other transactions that were processed at the same time as yours by clicking on the block number.  

<img alt="block explorer" src="https://user-images.githubusercontent.com/83733789/119708053-1a526780-be19-11eb-9be9-0daba50c9705.png" width=75%>

Now let's go back and look at the gas fees required for our transaction. There are three values of gas that are relevant to each transaction: gas limit, gas used, and gas price. 

The gas limit is a safety mechanism to protect users from potential errors. It sets a maximum amount of gas that a transaction can use to prevent situations where a transaction uses up the entire balance of a wallet. More complex transactions will require more gas and have a higher gas limit.  

The gas used value is the actual amount of gas used to perform a transaction. This will always be less than or equal to the gas limit. All unused gas will be returned to the transaction sender after a transaction executes.  

The gas price value is the price per unit of gas paid for a transaction. You can think of it like the auction price for a train ticket: every transaction wants to be included in the next block, but only the highest bidders will be included. The average gas price will fluctuate with demand for block space, meaning higher traffic volume will equate to higher gas prices for a transaction to be included in a block.  

As a user, you can manually set the gas price and gas limit when performing a transaction.  

*What should I keep in mind when setting the gas price and gas limit?*

If you set the gas price too low, your transaction may never be included in a block. If the gas limit is too low, a transaction may not have enough gas to complete. When this happens, the transaction fails and no gas is returned. For now, it is recommended that you use the gas price and gas limits suggested by MetaMask for each transaction. 

---

## :email: How to send a transaction

There are two main types of transactions: transfers between user addresses and interactions with smart contracts. 

First, let's try sending a transaction between addresses. We can send some of our xDai to another wallet that we own by creating another account in MetaMask. Click on the multicolored avatar in your wallet and then select **Create New Account**. This new account is also linked to your seed phrase, but has a unique private key. Copy the address of your second account by tapping on it. To switch back to your first account, click on the multicolored avatar again. We will now send xDai to our other address using the **send** button in MetaMask. 

<img src="https://user-images.githubusercontent.com/83733789/119894417-cec3ba80-bef9-11eb-9818-10506109f1f0.png" alt="send button" width=25%>

Paste the address of the recipient(our other wallet). Set the amount to send to whatever you would like. Because each transaction on the network costs gas, it is not possible to send the full balance of your wallet. It is recommended to leave the gas price and limit as-is here, since the minimum gas limit is 21,000 gwei.  

<img src="https://user-images.githubusercontent.com/83733789/119894945-7b9e3780-befa-11eb-8365-5dd232a761da.png" alt="transaction activity view" widith=25%>

You can view the status of sent transactions under the **Activity** tab in MetaMask. Tapping on it will show more details about the transaction and provide a link to the transaction hash on the blockchain explorer. 

> This method of sending transactions was used to demonstrate how to send cryptocurrency to other wallets. If you would like to transfer crypto between two accounts in the same extension or app, you can use the **Transfer between my accounts** function under after pressing **Send** as well. 

Another way to send and recieve crypto with MetaMask is to use QR codes. 


Let's send a transaction to a contract. 
