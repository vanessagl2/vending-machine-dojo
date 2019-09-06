# 8. Exact Change Only
<i>As a customer
<br>I want to be told when exact change is required
<br>So that I can determine if I can buy something with the money I have before inserting it
</i><br><br>When the machine is not able to make change with the money in the machine for any of the items that it sells, it will display EXACT CHANGE ONLY.


# 9. Sold Out products
<i>As a customer
<br>I want to be told when the item I have selected is not available
<br>So that I can select another item
</i><br><br>When the item selected by the customer is out of stock, the machine displays SOLD OUT. If the display is checked again, it will display the amount of money remaining in the machine or INSERT COIN if there is no money in the machine.

## Vending Machine: Example Input and Output
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