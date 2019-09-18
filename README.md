# vending-machine-dojo

This is a DOJO based on the Original Kata available at: 

https://github.com/guyroyse/vending-machine-kata

This codebase contains an extension for that DOJO


## Vending Machine Description
The goal of this program is to model a vending machine and the state it must maintain during it's operation. How exactly the actions on the machine are driven is left intentionally vague and is up to the implementor.
The machine works like all vending machines: it takes money then gives you items. 

The vending machine accepts money in the form of some coins: nickels ($0.05), dimes ($0.10), quarters ($0.25), and paper dollars($1). You must have at least have 3 primary items that cost $0.50, $0.65, $1.00. The user may hit a "coin return" button to get back the money they've entered so far. If you put more money in than the item's price, you get change back.

## Valid set of actions on the vending machine
* <b>NICKEL</b>(N: 0.05), <b>DIME</b>(D: 0.10), <b>QUARTER</b>(Q: 0.25),  <b>DOLLAR</b>(DO: 1.00) - insert money
* <b>COIN RETURN</b> - returns all inserted money
* <b>GET-CHIPS</b>, <b>GET-CANDY</b>, <b>GET-COLA</b> - select item CHIPS ($0.50), CANDY ($0.65),  COLA($1), or 
* <b>SERVICE</b> - a service person opens the machine and sets the available change and items

## The valid set of responses from the vending machine
* <b>N</b>, D</b>, Q</b>, DO - return money
* <b>COLA</b>, <b>CHIPS</b>, <b>CANDY</b> - the items sold

## The vending machine must track the following state:
* available items - each item has a count, a price, and a selector (COLA, CHIPS, CANDY)
* available change - # of nickels, dimes and quarters available
* currently inserted money


## Features
There are several features and their following inputs and outputs examples. 
If you want to develop a learning program based on those features please follow. 

* [Set 1: Modelling your Vending Machine](/vending-machine-features/features-set1.md)
* [Set 2: Add behaviours and setup the Vending Machine](/vending-machine-features/features-set2.md)
* [Set 3: Handle change and sold out products](/vending-machine-features/features-set3.md)
* [Set 4: Building an API to serve your Vending Machine](/vending-machine-features/features-set4.md)


