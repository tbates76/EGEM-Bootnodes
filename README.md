# EGEM-Bootnodes
- List of EGEM bootnodes.

Please submit your bootnodes to strengthen the EGEM network.

How do i find my bootnode address?

When you boot up go-egem there is a line that looks like this:


- self=enode://02cae3b86ae74b64b8766bb177ff4578cc51a18ad5b1b3df1304faef5e39bcb928d3308ca9991ef8aeedc5b7124eb0dca7b0bc74a5f682b13662a98112426057@[::]:30666

You remove the self= and then inside of the [::] at the end you replace it with your outside IP address.

So it should look something like this when done:

- enode://02cae3b86ae74b64b8766bb177ff4578cc51a18ad5b1b3df1304faef5e39bcb928d3308ca9991ef8aeedc5b7124eb0dca7b0bc74a5f682b13662a98112426057@[154.34.678.12]:30666


Where do i put the static-nodes.json file?

```<datadir>/egem/static-nodes.json```

```~/live-net/egem/static-nodes.json```

# How to update node list.

Turn off the node then use the command.

```rm -r ~/live-net/egem/static-nodes.json```

Then use this to update the list.

``` cd ~/live-net/egem/ && wget https://raw.githubusercontent.com/TeamEGEM/EGEM-Bootnodes/master/static-nodes.json ```

Then a just start the node back up with this command.

```cd ~/go-egem && screen -dmS go-egem /root/go-egem/build/bin/egem --datadir ~/live-net/ --maxpeers 100 --rpc```
