# 4. Make Change
<i>
As a vendor<br>
I want customers to receive correct change<br>
So that they will use the vending machine again<br>
</i>
<br>

When a product is selected that costs less than the amount of money in the machine, then the remaining amount is placed in the coin return.

# 5. Accept dollar
<i> As a vendor
<br>I want my machine to take one dollar in cash
<br>So that I sell with more options
</i>
<br><br>The machine will accept a new type of "money" which is 1 Dollar in paper. (Represented with the symbol DO)

# 6. Setup Money
<i>As a vendor
<br>I want to setup the current money amount
<br>So that I sell correctly
</i>
<br><br>When the vendor starts the day, the first thing they want to do is to setup the correct amount of money in the machine. That amount of money will be the base for all currency transactions in the machine. The operation for setting up the amount must be the first thing displayed on the machine when it is turned on. It is also an option that the vendor can access throughout the day. If the machine is turned down, then the amount is lost.


# 7. Setup products
<i>As a vendor
<br>I want to setup the current products amount
<br>So that I sell correctly
</i><br><br>When the vendor starts the day, after they setup the correct amount of money in the machine, they will setup the amount of products. That amount of products will be the base for all transactions in the machine. The operation for setting up the amount must be displayed on the machine when it is turned on. It is also an option that the vendor can access throughout the day. If the machine is turned down, then the amount is lost. 

## Vending Machine: Example Input and Output
#### Setting up machine when it is turned on in the first time
```
$ CURRENT BALANCE IS 0. SETUP IS REQUIRED
> SETUP-MONEY: DO, Q, DO, DO ,Q, Q, D, D, N
Current balance is $4.00: D, DO, DO, DO, Q, Q, Q, N

$ CURRENT AMOUNT OF PRODUCTS ARE []. SETUP IS REQUIRED
> SETUP-PRODUCTS: CANDY, CANDY, CHIPS, CANDY, CANDY, CHIPS, CHIPS, COLA, COLA
Current products are: 4 CANDY, 3 CHIPS, 2 COLA

$ INSERT COIN AND PRODUCT
```
