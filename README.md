# ZEOS Demo

Setup `cleos`:
```
wget https://github.com/AntelopeIO/leap/releases/download/v4.0.4/leap_4.0.4-ubuntu22.04_amd64.deb
sudo dpkg -i leap_4.0.4-ubuntu22.04_amd64.deb
# The following command should print: v4.0.4-7e1ad13e1e98b1e0703d0ea072b4fca5419cfdbe
cleos version full
```

Setup `zeos-cli`:
```
wget ...
# start the CLI interface by executing:
./zeos-cli
# print the public permission to import it into cleos:
alias authority
# copy the private key and exit
exit
```

Create `cleos` wallet:
```
cleos wallet create --to-console
# Save your wallet password in a save location!
cleos wallet import
# paste the private key of the public permission and hit Return
# create a new keypair for your UX testnet account
cleos create key --to-console
# save your private key in a safe location
cleos wallet import
# paste your private key to import
```

Create UX testnet account (using https://t.me/ux_testnet_faucet_bot):
```
# hit 'Start' and follow the instructions. Use the public key of the newly generated keypair above to set up your account
create account <account_name> <public_key>
# send some UTX/UTXRAM tokens into your new account
send utx to <account_name>
send utxram to <account_name>
```

ZEOS Faucet:
```
https://faucet.zeos.one/?user=<account_name>
```

Create ZEOS wallet:
```
./zeos-cli
wallet create
# type in wallet details and that's it!
exit
```

Send tokens from your testnet account into your ZEOS wallet:
```
# always make sure you have your cleos wallet unlocked before you use the ZEOS CLI
cleos wallet unlock
# copy & paste your cleos wallet password from above
./zeos-cli
wallet unlock
# you can just hit Enter here as the password check is still disabled
wallet move
# type in your testnet account name from above to exchange assets between that account and you ZEOS wallet
+ 1000 ZEOS 'first ZEOS UTXO'
+ 1000 ZEOS 'second ZEOS UTXO'
+ 100 UTX 'and some UTX'
# hit Enter twice if you're done with the list
# use '-' in the above notation to move assets in the other direction (from your ZEOS wallet back into your testnet account)
```


