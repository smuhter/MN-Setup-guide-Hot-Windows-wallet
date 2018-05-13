MASTERNODE GUIDE FOR WINDOWS

1.Open and Run the trittium-qt.exe wallet for the first time.  
2.Your firewall and antivirus might pop up to allow connection. Please allow the connections by making appropriate tick marks.
3.Wait for full wallet synchronizing with network. If there is a problem synchronizing, it may say “No Block Source Available” instead. If this happens, just close and re-open the wallet until it synchronizes. 
4.Go to Tools -> Debug Console.
5.In the Console window enter "getaccountaddress MN1" and copy the result. This is your MASTERNODE DEPOSIT ADDRESS, where you will deposit the coins to create a masternode. Pay 50000 TRTT exactly into this address. No more, no less.
-·Wait for 1 confirmation of the transaction.
6.In the Console Debug window enter "masternode genkey" and copy the result. This is your MASTERNODEPRIVKEY.
7.In the Console Debug window enter "masternode outputs" and copy the result. "txhash" is your YOURTXID. "outputidx" is YOUROUTPUTIDX
8.Open Configuration File in Notepad. This config file is located at C:/users/***Your windows username***/appdata(hidden)/roaming/trittium (or custom path, that you choice when first install wallet)   Then paste in the following.

rpcuser=YOURUSERNAME <br />
rpcpassword=YOURPASSWORD <br />
rpcallowip=127.0.0.1 <br />
rpcport=30002 <br />
port=30001 <br />
server=1 <br />
listen=1 <br />
daemon=1 <br />
masternode=1 <br />
masternodeaddr=YOUR_PUBLIC_IP:30001 <br />
masternodeprivkey=MASTERNODEPRIVKEY <br />

9.Now save and close the config file. 
10. Open Masternode.conf. This config file is located at C:/users/***Your windows username***/appdata(hidden)/roaming/trittium/masternode.conf  Then paste in the following.

MN1 YOURIP:30001 MASTERNODEPRIVKEY YOURTXID YOUROUTPUTIDX

11. Now save and close masternode.conf
12. Close the wallet by going to File -> Exit.
Open the Trittium Wallet again by running trittium-qt.exe. This is how you will always start the wallet going forward.
13. Wait for 15 confirmations of the transaction of 50000 coins.
Go to Masternodes Tab and start your Masternode by click in Start all or Start alias . You will see the response “Masternode started successfully”. Congratulations, your masternode is now running.
Now click the Masternodes tab that is now visible. You should see your new masternode appear in the list with the status ENABLED.
All masternodes need to be active for a certain amount of blocks before they are recognized by the network and eligible for rewards.
Warning!!!!  Wallet must be alwaysON!!! 