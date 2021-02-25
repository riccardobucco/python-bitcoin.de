# bitcoinde

Python wrapper for the [bitcoin.de trading API](https://www.bitcoin.de/en/api/tapi/doc). Currently, only v4 is supported (i.e., the latest version).

## Installation

Binary installers for the latest released version are available at the [Python Package Index (PyPi)](https://pypi.org/project/bitcoinde/):

    pip install bitcoinde

## Getting started tutorial

API endpoints require user authentication. Therefore, you must setup API access within your [account settings](https://www.bitcoin.de/en/userprofile/tapi) before using this package.

    from bitcoinde import TradingAPI

    client = TradingAPI(API_KEY, API_SECRET)
    client.show_orderbook('btceur', 'buy', seat_of_bank=['DE', 'IT'])
