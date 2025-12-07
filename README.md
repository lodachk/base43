# base43
Tracking Gas Price Trends on Base Using Python  Base gas fees change dynamically depending on L1 congestion and L2 activity. Tracking historical gas values helps you understand network health and find optimal deployment times.
Python example
from web3 import Web3
import time

w3 = Web3(Web3.HTTPProvider("https://mainnet.base.org"))

gas_values = []
for _ in range(10):
    gas = w3.eth.gas_price
    gas_values.append(gas)
    print("Gas:", gas)
    time.sleep(1)
