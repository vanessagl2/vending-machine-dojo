# vending-machine-dojo
This is a simple starter project for the Vending Machine Dojo. 
This is based on the Original Kata available at: 

https://github.com/guyroyse/vending-machine-kata




##Vending Machine Description
The goal of this program is to model a vending machine and the state it must maintain during it's operation. How exactly the actions on the machine are driven is left intentionally vague and is up to the implementor.
The machine works like all vending machines: it takes money then gives you items. 

The vending machine accepts money in the form of some coins: nickels ($0.05), dimes ($0.10), quarters ($0.25), and paper dollars($1). You must have at least have 3 primary items that cost $0.50, $0.65, $1.00. The user may hit a "coin return" button to get back the money they've entered so far. If you put more money in than the item's price, you get change back.

##Valid set of actions on the vending machine
* <b>NICKEL</b>(N: 0.05), <b>DIME</b>(D: 0.10), <b>QUARTER</b>(Q: 0.25) - insert money
* <b>COIN RETURN</b> - returns all inserted money
* <b>GET-CHIPS</b>, <b>GET-CANDY</b>, <b>GET-COLA</b> - select item CHIPS ($0.50), CANDY ($0.65),  COLA($1), or 
* <b>SERVICE</b> - a service person opens the machine and sets the available change and items

##The valid set of responses from the vending machine
* <b>NICKEL</b>, DIME</b>, QUARTER</b> - return coin
* <b>COLA</b>, <b>CHIPS</b>, <b>CANDY</b> - the items sold

##The vending machine must track the following state:
* available items - each item has a count, a price, and a selector (COLA, CHIPS, CANDY)
* available change - # of nickels, dimes and quarters available
* currently inserted money

##Vending Machine: Example Input and Output
<b>Example 1: Buy Cola with exact change</b>
```
$ INSERT COIN AND PRODUCT
> Q, Q, Q, Q GET-COLA
COLA
```

<b>Example 2: Start adding change but hit coin return to get change back</b>
```
$ INSERT COIN AND PRODUCT
> Q, Q, COIN-RETURN
Q, Q
```