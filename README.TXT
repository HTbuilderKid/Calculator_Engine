
22. Well, the line about ("All tests passed") is hardcoded text, and the method never actually checks whether the results are correct, it just prints the message after running the tests. Even if the calculations were wrong, it would still print the same text

23. Following the logic of the source code for testPlus(), the result should always be 7, since every time we call the method, it would clear the engine before doing the calculations. 3 + 4 = 7. The result, when I tested, was also 7

24. The same logic as 23, and the answer we get is 5. 9 - 4 = 5. The logic is right, and the test shows that the output is also correct.

25. When inspecting the logic, I noticed that equals() assumes that if previousOperator isn't +, it's -, which means that any other operator will de defaulted to substraction (including space). 
