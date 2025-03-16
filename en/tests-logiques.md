# Logic tests 

* [VERSION FRANÇAISE](../fr/tests-logiques.md)
  
## ⚔️ =IF( function 

It is used to perform a logic test. If the test is successful, the cell will display a predefined value; if the test fails, the cell will display another value.

> **=IF(** logical test ; value if TRUE ; value if FALSE )



<center> <img width=200 src="images/fonction_si.JPG" alt="Example 1" /> </center>

<center> <i>Example 1</i> </center>

For example, to check whether the cells in column A are positive or negative, enter the first cell in column B :

~~~ =IF(A1>0; "Positive"; "Negative") ~~~

Then "drag" the cell so that the formula is applied to all the cells in column B.


<center> <img width=200 src="images/moyenne.JPG" alt="Example 2" /> </center>

<center> <i>Example 2</i> </center>

I want to know if my semester is validated. To do this, I calculate my average: it's my logical test. Two results are possible: either I have the average, so the test passes and I validate my semester (this is the value if TRUE), or I don't have the average, so the test fails and I don't validate my semester (this is the value if FALSE).

~~~ =IFAVERAGE(A1;A10)>=10; "Semester validated"; "Semester not validated") ~~~

* * *


## ⚔️ =AND( and =OR( functions 

These functions return "TRUE" or "FALSE" depending on the conditions met. For the AND function, all conditions must be met to validate the test. For the OR function, only one of the conditions is required.</p>

> =AND( condition 1 ; condition 2 ; etc. ) =OR( condition 1 ; condition 2 ; etc. ) 



<center> <img width=500 src="images/fonction_etou.JPG" alt="Example 2" /> </center>

<center> <i>Example 3</i> </center>

For example, in a list of customers, we want to check who has placed at least 10 orders in column A, <b>and</b> who has spent more than €500 in column B, <b>and</b> who has validated their registration in column C.

~~~ =AND(A1>=10;B1>500;C1="YES") ~~~

If you want to check which customers have not validated any of these conditions, use this formula:

~~~ =OR(A1<10;B1<500;C1="NO") ~~~



AND/OR formulas can be nested within an IF function to create more complex tests that depend on a greater number of conditions. In this way, we use the "TRUE" or "FALSE" condition checking of AND/OR functions to program a suitable IF function.

> =IF(AND( condition 1 ; condition 2 ; etc. ) ; value if **all is TRUE** ; value if **ONE is FALSE** ) =IF(OR( condition 1 ; condition 2 ; etc. ) ; value if **ONE is TRUE** ; value if **all is FALSE** )



In example 3, if we want only customers who have met <b>all</b> the conditions to receive a 25% discount on their order in column E, we enter the following formula:

~~~ =IF(AND(A1>=10;B1>500;C1="YES");E1\*0.75;E1) ~~~

If we want all customers meeting <b>at least one</b> condition to receive a 10% discount, we use this formula:

~~~ =IF(OR(A1<10;B1<500;C1="NO");E1;E1\*0,90) ~~~


* * *

<center> <b>If you want the logic test to have three or more possible results, there are several solutions: </b> </center> </p> <br>

## ⚔️ =IF( nested function

An IF function can be nested within another IF function to create a subordinate relationship between several logical tests.

> =IF( logical test X ; IF( logical test Y ; **value 1** if Y TRUE ; **value 2** if Y FALSE ) ; **value 3** if X FALSE )

Here, we perform a first logical test (X). If true, a second logical test (Y) is performed to differentiate between two results. If it fails, a third result is returned.

In example 1, if we want registered customers to have a 25% discount on their order in column E if they have spent more than 500€ and a 15% discount otherwise, and if we want non-registered customers to have a 5% discount whatever the amount they have spent, we write:

~~~ =IF(C1="YES";IF(B1>500;E10;75;E10,85);E1\*0,95) ~~~



## ⚔️ =IF.CONDITIONS( function 

If you want to perform different logical tests with a large number of possible results, use this function:

> =IF.CONDITIONS( logical test X ; **value 1** if TRUE ; logical test Y ; **value 2** if TRUE ; logical test Z ; **value 3** if TRUE )



<p>In example 3, to check whether the cells in column A are positive, negative or equal to zero, enter the first cell in column B: </p>
<pre>=IF.CONDITIONS(A1>0; "Positive";A1=0; "Zero";A1&lt;0; "Negative")</pre>



## ⚔️ =IF.MULTIPLE( function 

There's another IF function, which tests the value of a particular cell. It works by pairs of values and results for each possibility, with a default result.

> =IF.MULTIPLE( cell to check ; value 1 ; result 1 ; value 2 ; result 2 ; value 3 ; result 3 ; default result )



For example, we have a list of athletes in column A and we want to identify the winners of the competition:

~~~ =IF.MULTIPLE(A1;1; "Gold medal";2; "Silver medal";3; "Bronze medal"; "Off podium") ~~~


* * *

<center> <a href="premiers-pas" target="_self" title="First steps"> <font color="#389E46"> &lt;&lt; First steps - Previous page </font> </a> &lt;&lt; - ⚔️ - >> <a href="mise-en-forme-conditionnelle" target="_self" title="Conditional formatting"> <font color="#389E46"> Next page - Conditional formatting >> </font> </a> </center>
