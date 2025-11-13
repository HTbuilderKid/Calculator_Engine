
22. Well, the line about ("All tests passed") is hardcoded text, and the method never actually checks whether the results are correct, it just prints the message after running the tests. Even if the calculations were wrong, it would still print the same text

23. Following the logic of the source code for testPlus(), the result should always be 7, since every time we call the method, it would clear the engine before doing the calculations. 3 + 4 = 7. The result, when I tested, was also 7
