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

## TradingAPI methods

You can find more info about available endpoints and parameters int the [bitcoin.de trading API docs](https://www.bitcoin.de/en/api/tapi/doc). More methods will be implemented very soon!

- `show_orderbook(trading_pair: str, type: str, **get_params)`
  
  Search the order book for suitable offers
- `show_order_details(trading_pair: str, order_id: str)`

  Get details about an offer

- `show_my_orders(self, trading_pair: Optional[str] = None, **get_params)`

  Retrieving and filtering my orders
- `show_my_order_details(trading_pair: str, order_id: str)`

  Call up details about one of my orders
- `show_orderbook_compact(trading_pair: str)`

  Buy and sell offers (bids and asks) in a compact form
- `show_my_trade_details(trading_pair: str, trade_id: str)`

  Get details about a trade
- `show_my_trades(trading_pair: Optional[str] = None, **get_params)`

  Retrieving and filtering my trades
- `show_public_trade_history(trading_pair: str, **get_params)`

  Successfully completed trades
- `show_account_info()`

  Calling up account information
- `show_rates(trading_pair: str)`

  Query of the weighted average rate for the last 3 hours and the last 12 hours
- `show_account_ledger(currency: str, **get_params)`

  Calling up the account statement
- `show_permissions()`

  Provides all actions for which the API key used for the request is activated
- `show_deposit(currency: str, deposit_id: str)`

  Get details of a deposit
- `show_deposits(currency: str, **get_params)`

  Retrieving Deposits
- `show_withdrawal(currency: str, withdrawal_id: str)`

  Get details of a payout
- `show_withdrawal_min_network_fee(currency: str)`

  View the current minimum network fee for a payout
- `show_withdrawals(currency: str, **get_params)`

  Getting Payouts
