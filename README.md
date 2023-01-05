
Need to install:
1) Minimum knowledge of Linux (and Linux itself)
2) `jq`
3) `idena-go` (place in script folder, or change script)
4) `idena-desktop` (if validating, put in `/bin/`)
5) `curl` (but it is often preinstalled)

You unpack, make the files `restart_testnet` and `start_client` executable. You run everything while in this folder.
Above in the `restart_testnet` file, you can change the standard API key that all nodes will have and the number of minutes until the first validation.
In the `conf_*.json` files at the bottom there are validation duration settings and all that. They can be changed very carefully before restarting in both files.
Clients can be started with `./start_client node2` command, or with any other node folder that will be created.

For start:
1) Add as many addresses and keys as you need to the `keys` file. Now there are enough keys for 6 nodes.
2) Run `./restart_testnet 6`, or how many nodes you need. The nodes should start up and connect. There will be 1 god node and the rest are normal.
3) If validation is needed, then you need to wait until the `invites` file is created, open it and activate all nodes with these invites (including the god node)
4) When the god node becomes a candidate, create one flip on its behalf.
5) Validate on all nodes.

