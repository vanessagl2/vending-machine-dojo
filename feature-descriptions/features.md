#Accept Coins
<i>
As a vendor<br>
I want a vending machine that accepts coins<br>
So that I can collect money from the customer<br>
</i>
<br>

The vending machine will accept valid coins (nickels, dimes, and quarters) and reject invalid ones (pennies). When a valid coin is inserted the amount of the coin will be added to the current amount and the display will be updated. When there are no coins inserted, the machine displays INSERT COIN. Rejected coins are placed in the coin return.

#Select Product
<i>
As a vendor<br>
I want customers to select products<br>
So that I can give them an incentive to put money in the machine<br>
</i>
<br>

There are three products: cola for $1.00, chips for $0.50, and candy for $0.65. When the respective button is pressed and enough money has been inserted, the product is dispensed and the machine displays THANK YOU. When the display is checked again, it will display INSERT COIN and the current amount will be set to $0.00. If there is not enough money inserted then the machine displays PRICE and the price of the item and subsequent checks of the display will display either INSERT COIN or the current amount as appropriate.


#Return Coins
<i>
As a customer<br>
I want to have my money returned<br>
So that I can change my mind about buying stuff from the vending machine<br>
</i>
<br>

There are three products: cola for $1.00, chips for $0.50, and candy for $0.65. When the respective button is pressed and enough money has been inserted, the product is dispensed and the machine displays THANK YOU. When the display is checked again, it will display INSERT COIN and the current amount will be set to $0.00. If there is not enough money inserted then the machine displays PRICE and the price of the item and subsequent checks of the display will display either INSERT COIN or the current amount as appropriate.


#Make Change
<i>
As a vendor<br>
I want customers to receive correct change<br>
So that they will use the vending machine again<br>
</i>
<br>

When a product is selected that costs less than the amount of money in the machine, then the remaining amount is placed in the coin return.

#Accept dollar
<i> As a vendor
<br>I want my machine to take one dollar in cash
<br>So that I sell with more options
</i>
<br><br>The machine will accept a new type of "money" which is 1 Dollar in paper. (Represented with the symbol DO)

#Exact Change Only
<i>As a customer
<br>I want to be told when exact change is required
<br>So that I can determine if I can buy something with the money I have before inserting it
</i><br><br>When the machine is not able to make change with the money in the machine for any of the items that it sells, it will display EXACT CHANGE ONLY.

#Sold Out products
<i>As a customer
<br>I want to be told when the item I have selected is not available
<br>So that I can select another item
</i><br><br>When the item selected by the customer is out of stock, the machine displays SOLD OUT. If the display is checked again, it will display the amount of money remaining in the machine or INSERT COIN if there is no money in the machine.
