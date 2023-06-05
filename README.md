# bungee_refuel
Software to bungee refuel by multiple accounts
# Bungee fuel
[Bungee fuel](https://www.bungee.exchange/refuel) - a convenient bridge for bridge native tokens between networks with a small commission.

  - Supported networks in script: *Arbitrum, Avalanche, BSC, Polygon, Fantom*
 
**P.S. Before using, be sure to check on the site itself whether it is possible to bridge the number of tokens that you want. Basically it's just a frontend limit and should transfer any amount, on **your own risk** as they say.**
 
  <a href="https://imgbb.com/"><img src="https://i.ibb.co/z45TTVv/bungee.png" alt="bungee" border="0"></a <br/>
## Setting
  The script is run through the file `start_refuel.py`
  All settings are made in the `config.py` file:
 
  - **SOURCE_CHAIN** - the network from which we will bridge the native token
  - **DESTINATION_CHAIN** - the network to which we bridge and replenish the native token
  - **MIN_NATIVE_AMOUNT_OUT and MAX_NATIVE_AMOUNT_OUT** - a random number for the bridge will be selected between these two values, if you do not need random, specify the same numbers in both fields
  - **MIN_DELAY_SECONDS and MAX_DELAY_SECONDS** - a random number will be selected between these two values, which will be the delay in seconds between accounts (wallets)
  - **MAX_GAS_LIMIT** - each network needs a different gas limit, but you can set a large value in advance, in the end, the value required by the network will be used through gas_estimate
  - **TEST_MODE** - Can be run in test mode, the script will check the correctness of the transaction and show the estimate gas

## RPC setup
All rpc urls are in `rpcs.json` where they can be changed/changed

## Wallets
All privates are inserted into the file from a new line in the `wallets.txt` file (format is only 0x123...), if the file does not exist, it will be created automatically after the first launch

## Launching and using
Before starting via pip, install the necessary libraries:

     pip install -r req.txt
   Running the script:
  

     python start_refuel.py
