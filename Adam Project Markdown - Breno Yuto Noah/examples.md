<style>@import url("//readme.codeadam.ca/readme.css");</style>

**<p style="text-align: center;">Sample Pseudocode</p>**

"Adequate"  

FOR X = 1 to 10  
  FOR Y = 1 to 10  
    IF gameBoard[X][Y] = 0  
      Do nothing  
    ELSE  
      CALL theCall(X, Y) (recursive method)  
      increment counter  
    END IF  
  END FOR  
END FOR

"Better"

Set moveCount to 1  
FOR each row on the board  
  FOR each column on the board  
    IF gameBoard position (row, column) is occupied THEN  
      CALL findAdjacentTiles with row, column  
      INCREMENT moveCount  
    END IF  
  END FOR  
END FOR

(Note: the logic is restructured to omit the "do nothing" clause)

___
<br>
"Not So Good"
<br><br>

FOR all the number at the back of the array  
  SET Temp equal the addition of each number  
  IF > 9 THEN  
    get the remainder of the number divided by 10 that index  
    and carry the "1"  
  Decrement one  
Do it again for numbers before the decimal  
<br>
 

"Good Enough (not perfect)"

SET Carry to 0  
FOR each DigitPosition in Number from least significant to most significant

COMPUTE Total as sum of FirstNum[DigitPosition] andSecondNum[DigitPosition] and Carry
  
  IF Total > 10 THEN  
    SET Carry to 1  
    SUBTRACT 10 from Total  
  ELSE  
    SET Carry to 0  
  END IF  

STORE Total in Result[DigitPosition]

END LOOP  

IF Carry = 1 THEN  
  RAISE Overflow exception  
END IF

___
<br>
"Pretty Good"  This example shows how pseudocode is written as comments in the source file. Note that the double slashes are indented.
<br><br>

public boolean moveRobot (Robot aRobot)  
{  
  //IF robot has no obstacle in front THEN  
    // Call Move robot  
    // Add the move command to the command history  
    // RETURN true  
  //ELSE  
    // RETURN false without moving the robot  
  //END IF  
}  

Example Java Implementation

<li>source code statements are interleaved with pseudocode.</li> 
<li>comments that correspond exactly to source code are removed during coding.</li><br>


public boolean moveRobot (Robot aRobot)  
{  
  //IF robot has no obstacle in front THEN  
  if (aRobot.isFrontClear())  
  {  
    // Call Move robot  
    aRobot.move();  
    // Add the move command to the command history  
    cmdHistory.add(RobotAction.MOVE);  
    return true;  
  }  
  else // don't move the robot  
  {  
    return false;  
  }//END IF  
}  





___
<br>
Document History
<br>

<style>
table {
  width: 100%;
}

th, td {
  border: 1px solid black;
}
</style>

| Date           | Author| Change |
| :---------------- | :------ | :---- |
| 12/2/03        |   JD  | Added Exception Handling and more examples |
| 2/21/03           |   JD   | Added "problem domain vocabulary"paragraph.<br>Modified FOR loop explanation. |

<br>
<br>

---
---
<br>

**Vague Pseudocode examples**

These are examples of pseudocde which are written too vaguely.

___

#1
Assumptions:  Deck is an abstraction of queue that can be shuffled, and player's hand is an abstraction of List.
Create the scenario by picking 3 random cards from the deck.

Remove those three cards from the deck.

Randomly distribute the remaining cards from the deck to each player.

___

#2

State your assumpions about data structures.

IF evidence is relevant to the hypothesis presented THEN  
  RETURN TRUE  
END IF

___

#3

IF the player is disconnected THEN

The computer determines the refutation

ELSE

Send suggestion to player

END IF

___

#4

Increment turn order number.

Determine which player in the players array the incremented turn order number corresponds to.

___
___

On the other hand, here is an example that is too specific.  

FOR i = 1 to 24 LOOP  
    Add Rainfall[i] to Total  
END LOOP  

It would be better to express the loop as "FOR each hour of the day LOOP"
 

<div style="text-align: center; display: flex; justify-content: center; margin-top: 30px">

[Previous](exceptionhandle.md)

</div>

<div style="text-align: center; text-decoration: underline; text-decoration-color: #3486E3; margin-top: 150px;" markdown="1">

[Home](home.md)     
[What is Pseudocode?](what-is.md)  
[If-Then-Else](if-then-else.md)  
[While](while.md)  
[Case](case.md)
[Repeat-Until](repeat-until.md)  
[For](for.md)  
[Nested-Constructs](nested.md)  
[Subprocedures](subprocedures.md)  
[Exception-Handling](exceptionhandle.md)  
[Examples]  
<div>


---
Excerpted from the original at https://users.csc.calpoly.edu/~jdalbey/SWE/pdl_std.html

---

<a href="https://brickmmo.com">
<img src="https://brickmmo.com/images/brickmmo-logo-horizontal.jpg" width="100">
</a>

