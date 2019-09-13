# 1. Accept Coins
<i>
As a vendor<br>
I want a vending machine that accepts coins<br>
So that I can collect money from the customer<br>
</i>
<br>

The vending machine will accept valid coins (nickels, dimes, and quarters) and reject invalid ones (pennies). When a valid coin is inserted the amount of the coin will be added to the current amount and the display will be updated. When there are no coins inserted, the machine displays INSERT COIN. Rejected coins are placed in the coin return.

# 2. Select Product
<i>
As a vendor<br>
I want customers to select products<br>
So that I can give them an incentive to put money in the machine<br>
</i>
<br>

There are three products: cola for $1.00, chips for $0.50, and candy for $0.65. 
When the respective button is pressed and enough money has been inserted, 
the product is dispensed. 
When the display is checked again, it will display INSERT COIN and the current amount will be set to $0.00. 
If there is not enough money inserted then the machine displays PRICE and the price of the item and subsequent checks of the display will display either INSERT COIN or the current amount as appropriate.


# 3. Return Coins
<i>
As a customer<br>
I want to have my money returned<br>
So that I can change my mind about buying stuff from the vending machine<br>
</i>
<br>

There are three products: cola for $1.00, chips for $0.50, and candy for $0.65. When the respective button is pressed and enough money has been inserted, the product is dispensed. When the display is checked again, it will display INSERT COIN and the current amount will be set to $0.00. If there is not enough money inserted then the machine displays PRICE and the price of the item and subsequent checks of the display will display either INSERT COIN or the current amount as appropriate.


## Vending Machine: Example Input and Output
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
