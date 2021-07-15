# group-purchase

Alice, Bertrand, Clara and Desmond often make group purchases. They keep the list of their purchases in a csv file like this one:

```
item,unitp,qty,amount,buyer
pencils           ,  0.50 , 20  ,  10.00 , Bertrand
paper             ,  1.50 , 25  ,  37.50 , Alice
paper             ,  1.80 , 50  ,  90.00 , Desmond
laundry detergent ,  2.00 , 10  ,  20.00 , Clara
trash bags        ,  4.30 , 100 , 430.00 , Clara
gift cards        ,  8.00 , 1   ,   8.00 , Bertrand
lightbulbs        ,  1.00 , 10  ,  10.00 , Clara
~ shipping        , 40.00 , 1   ,  40.00 ,
~ total           ,       ,     , 645.50 ,
```

The last lines of the file contain the shipping fee and the grand total. Their `item` field begins with a `~`.

The shipping fee is not split into equal parts between buyers: rather it is attributed to each member in proportion to their purchase amount. In the example above, the total _without shipping_ is 605.50. Clara's purchases amount to 460.00 so her part of the shipping fee is 460.00 / 605.50 = 30.38, making her total part of the bill 460.00 + 30.38 = 490.38.

Write a program that reads a CSV file like the one above and outputs a CSV file of each person's total like the one below:

```
buyer,amount
Alice    ,  39.98
Bertrand ,  19.19
Clara    , 490.38
Desmond  ,  95.95
~ total  , 645.50
```
Note that the amounts are rounded and adjusted so that their sum is equal to the grand total.


