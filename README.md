<h1 align="center"><br>
    <a href="https://perun.network/"><img src=".assets/go-perun.png" alt="Perun" width="196"></a>
<br></h1>

<h2 align="center">Perun Internet Computer Demo</h2>

This repository contains the Perun Internet Computer demo client, which utilizes the [go-perun](https://github.com/perun-network/go-perun) channel library, and also the [Internet Computer backend](https://github.com/perun-network/perun-icp-backend)

# Setup

Clone this repository:

```
  $ git clone https://github.com/perun-network/perun-icp-demo.git
```


Spin up the local Internet Computer (IC) replica, serving as a local testnet for demonstration purposes.

```
  $ ./startdeploy.sh
```

This will start the IC replica in the background and deploy the two canisters you need for the demo: The Ledger canister, and the Perun Payment channel canister. The Ledger canister allows us to transfer assets on the IC and the Perun canister implements the Payment Channel logic. You can find the source code for the Perun canister [here](https://github.com/perun-network/perun-icp-canister).

# Using the demo

You can start the demo by simply running

```
  $ go run main.go
```
The accounts used in the demo are located in `/userdata/identities` and are pre-funded in the script `startdeploy.sh`. 

You will be greeted with a demo window that is split into two panes. You can play around with the different functions of the demo by using the keybinds listed below.

## Keybinds

* `ctrl+a`: Select left pane
* `ctrl+b`: Select right pane
* `tab`: Cycle through selectable fields
* `Enter`: Select or confirm highlighted field
* `r`: Go back to parent page
* `q`: Close the demo


## Exiting the demo

You can exit the demo by pressing `q` at any time. Afterwards, you need to stop the IC replica by running

```
  $ ./stopdfx.sh
```

## Copyright

Copyright 2023 PolyCrypt GmbH. Use of the source code is governed by the Apache 2.0 license that can be found in the [LICENSE file](LICENSE).