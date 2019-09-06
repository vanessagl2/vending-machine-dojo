# vending-machine-dojo
This is a simple starter project for the Vending Machine Dojo. 
This is based on the Original Kata available at: 

https://github.com/guyroyse/vending-machine-kata




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

[Set 1: Modelling your Vending Machine](/feature-descriptions/features-set1.md) 

## Vending Machine: Example Input and Output
#### Buy Cola with exact change
```
$ INSERT COIN AND PRODUCT
> Q, Q, Q, Q, GET-COLA
COLA

$ INSERT COIN AND PRODUCT
```

#### Start adding change but hit coin return to get change back
```
$ INSERT COIN AND PRODUCT
> Q, Q, COIN-RETURN
Q, Q
```

#### Buy product without enough money and then insert money after
```
$ INSERT COIN AND PRODUCT
> Q, Q, Q, GET-COLA
PRICE: 1.00, BALANCE: 0.75
$ INSERT COIN OR HIT COIN-RETURN 
> Q, GET-COLA
COLA
```

#### Buy product without enough money and then give up on purchase
```
$ INSERT COIN AND PRODUCT
> Q, Q, Q, GET-COLA
PRICE: 1.00, BALANCE: 0.75
$ INSERT COIN OR HIT COIN-RETURN 
> Q, Q, COIN-RETURN
Q, Q, Q, Q, Q
```
#### Buy product without enough money and then add more than necessary
```
$ INSERT COIN AND PRODUCT
> Q, Q, Q, GET-COLA
PRICE: 1.00, BALANCE: 0.75
$ INSERT COIN OR HIT COIN-RETURN 
> D, D, D, GET-COLA
N, COLA
```

#### Setting up money in the machine when it is turned on in the first time
```
$ CURRENT BALANCE IS 0. SETUP IS REQUIRED
> SETUP-MONEY: DO, Q, DO, DO ,Q, Q, D, D, N
Current balance is $4.00: D, DO, DO, DO, Q, Q, Q, N

$ CURRENT AMOUNT OF PRODUCTS ARE []. SETUP IS REQUIRED
> SETUP-PRODUCTS: CANDY, CANDY, CHIPS, CANDY, CANDY, CHIPS, CHIPS, COLA, COLA
Current products are: 4 CANDY, 3 CHIPS, 2 COLA

$ INSERT COIN AND PRODUCT
```

#### Exact change only
```
$ EXACT CHANGE ONLY. INSERT COIN AND PRODUCT: 
> Q, Q, GET-CHIPS
CHIPS
```

```
$ EXACT CHANGE ONLY. INSERT COIN AND PRODUCT: 
> DO, GET-CHIPS
DO
$ EXACT CHANGE ONLY. INSERT COIN AND PRODUCT:
```

#### SOLD OUT product
```
$ INSERT COIN AND PRODUCT: 
> Q, Q, GET-CHIPS
Q, Q. CHIPS is SOLD OUT

$ INSERT COIN AND PRODUCT:
```