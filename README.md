# meteor-dapp-pricefeed
A MeteorJS price feed DApp - for operating price feeds on Ethereum.

<img src="app/public/images/screen.jpg" />

** Please note that this DApp is still in Alpha.

## <a name="installation"></a> Installation

1. Clone this repo

  `git clone https://github.com/SilentCicero/meteor-dapp-pricefeed.git`

2. Remove `.git`

  `cd meteor-dapp-pricefeed/app && rm -rf .git`

## <a name="deployment"></a> Deployment

Start an eth node open the http://localhost:3000 in *mist*, *mix* or *alethzero* or run a CPP node as follows:

    $ eth -j -b // for a mining node: $ eth -j -b -f -n no -m yes

Start your app using meteor

    $ cd meteor-dapp-pricefeed/app
    $ meteor

Go to http://localhost:3000/admin

  - click `'Deploy PriceFeed Contract'` and copy the new address

Edit client/lib/feedConfig.js

  - change `Feed.address` to the new address

Wait for mining, refresh, then start using the DApp!

## <a name="server"></a> Server Deployment

Edit server.py

  - change vars `CONTRACT_ADDRESS` and `OWNER_ADDRESS` to the appropriate values

Running the server

    $ cd meteor-dapp-pricefeed/app
    $ python server.py

## <a name="functionality"></a> DApp Functionality
- landing page
- admin page (a dashboard for contract owner)
- tracking page (to track subscriptions)
- can subscribe an address
- only subscribers can access the feed data
- renewable subscriptions
- owner can manage feed price, subscribers, subscription duration and payout balance
- a basic python server for updating the feed info

## <a name="layout"></a> Page Layout
- Landing page: /
- Admin page: /admin
- Tracking page: /track/0x00000

## <a name="about"></a> Soldity
Original SOL by Gavin Wood <g@ethdev.com>

## <a name="about"></a> About

This DApp is a starting point for deploying and operating price feeds on Ethereum. It could potentially be modified to meet the needs of almost any price feed. Presently, the default title is "Gold Price Today*" (which will be my gold price feed).

## <a name="todo"></a> TODO
- Decimal number support for feed info
- Multi-type feed data (e.g. "gold", "silver" etc.)
- Setup contact form (make active)
