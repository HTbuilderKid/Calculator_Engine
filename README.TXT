
22. Well, the line about ("All tests passed") is hardcoded text, and the method never actually checks whether the results are correct, it just prints the message after running the tests. Even if the calculations were wrong, it would still print the same text

23. Following the logic of the source code for testPlus(), the result should always be 7, since every time we call the method, it would clear the engine before doing the calculations. 3 + 4 = 7. The result, when I tested, was also 7

24. The same logic as 23, and the answer we get is 5. 9 - 4 = 5. The logic is right, and the test shows that the output is also correct.

25. When inspecting the logic, I noticed that equals() assumes that if previousOperator isn't +, it's -, which means that any other operator will de defaulted to substraction (including space). 

26. *Please refer to the screenshoot of the excel sheet in the repository :)*

27. If there is no previous operator (eg. we press = before pressing + or -, previousOperator will still be ' ', which means that the condition (if(previousOperator == '+')) is false, so the else runs, and does a subtraction by default.
(displayValue = leftOperand - displayValue;)
Since leftOperand was initially 0, this becomes displayValue = 0 - displayValue, which just flips the sign of whatever number was on the screen.
So applyPreviousOperator() is safer because there's a fallback for the case where there's no operator yet: 
else {
   // There was no preceding operator.
   leftOperand = displayValue;
}
This basically makes sure that if no operator was pressed, the engine just uses the number as-is. So the asnwer to 27 would simply be: pressing = without any operator would produce a wrong result

28. After calling clear(), the engine is not in the same state as it was after the first clear() because previousOperator is still '+', because the clear() just changes the current displayValue to 0, and doesn't change anything else
