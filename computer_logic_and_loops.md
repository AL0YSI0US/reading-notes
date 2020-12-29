Loop / While / For / Condition / Increment / Decrement

## Loop counters

for (var i = 0; < 10; i++) {        This is a **for** loop  the condition is a counter that counts to ten.

   document.write(i);               The result would write **"0123456789"** to the page.  
}

|  **Initialization** |  **Condition**  | **Update**  |
|  :----: |  :----:  | :----:  |
|  create a variable and set it to **0**. This variable is commonly called **i**, and it acts as the counter | the loop should continue to run until the counter reaches a specified counter.  | Every time the loop has run the statements in the curly braces, it adds one to the counter.  |
|  **var i = 0;** |   **i > 10;**   | **i++**  |
|  the variable is only created the first time the loop is run. variable (i) also referred to as *index* |  the value of **i** was initially set to **0**, so in this case the loopwill run 10 times before stopping.  | one is added to the counter using the (++) operator.  |

## Logical Operators 

|  **&& Logical And** |  **`||` Logical or**  | **Logical Not**  |
|  :----: |  :----:  | :----:  |
|  This operator tests more than one condition |  This operator tests at least one condition.  | This operator takes a single boolean value and inverts it.  |
|  ((2 < 5) && (3 >= 2)) |  ((2 > 5) `||` (2 < 1>) | !(2 < 1)  |
|  returns true |  returns true  | returns true  |
|  If both expressions evaluate to **true** then the expression returns **true**. If just one of these returns **false** |  If either expression evaluates to **true**, then the expression returns **true**. If both return **false**, then the expression will return **false**. then the expression will return **false**. | This reverses the state of an expression. If it was **false** (without the ! before it) it would return **true**. If the statement was **true**, it would return **false**. |
|  **true** && **true** returns **true** |  **true** `||` **true** returns **true**   |  !**true** return **false** |
|  **true** && **false** returns **false**  |   **true** `||` **false** returns **true**    |   !**false** returns **true**  |
|   **false** && **true**  returns **false**   |   **false** `||` **true** returns **true**    |   [intentionally blank]  |
|   **false** && **false** returns **false**   |   **false** `||` **false** returns **false**    |intentionally blank]  |

> ***Logical Operations*** are evaluated **left** to **right**. If the first condition can provide enough informationn to get the answer, then there is no need to evaluate the second condition. 

# Computer Logic and Loops

| ***Term*** | Context | 
|  :----: |  ----  |   
|  **Loop**  | loops check a condition. If it returns **true**, a code block will run. Then the condition will be checked again and if it still returns **true**, the code block will run again. It repeats until the condition returns **false**. *there are three common types of loops:* **for : while : do while**  | 
|  **for**  | If you need to run code a specific number of times, use a **for** loop. (it is the most common loop.) In a **for** loop,the condition is usually a counter which is used to tell how many times the loop should run. |
|  **while**  | If you do not know how many times the code should run, you can use **while** loop. Here the condition can be something other than a computer,and the code will continue to loop for as long as the condition is **true**. |
|  **do while**  | the **do...while** loop is very similar to the ***while*** loop, but has one key difference: it will always run the statements inside the curly braces at least once, even if the condition evaluates to **false**. |
|  **Loop Counters**  | a **for** loop uses a counter as a condition. This instructs the code to run a specified number of times. ***The condtion is made up of three statements:*** **initialization (ph1) : condtion (ph2): update (ph3)** |
|  **Condition**  | the loop should continue to run until the counter reaches a specified number.  |
|  **Increment**  | [guide](https://codeburst.io/javascript-increment-and-decrement-8c223858d5ed)  |
|  **Decrement**  | *see* [guide] *above*  |

**Read**

Duckett: JavaScript & jQuery:
+ Comparison and logical operators: 150-151, 156, and 157 
+ for and while loops: 170 - 173, and 176

[Code 102 Table of Contents](CodeFellows_102.md)

[<== Home](README.md) [Forward ==>](career_coaching.md)
