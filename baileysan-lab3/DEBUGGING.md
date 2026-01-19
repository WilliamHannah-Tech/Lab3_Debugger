# Debugging process Lab 03
### Troubleshooting & Debugging log

## pyton_app4.py file editing
- Line 16 Converted to int() to float() to cure:
```
num = float(stripped)
```
- Line 85, added ':' to `else` to cure  - else:

- Line 97 def flawed_function(x, y) `added ":" to cure the error` :
```
- def flawed_function(x, y):
```
- Ran the python file via command `python3 python_app4.py` and the output included `File not found: numbers.txt
```
 [Running]
/usr/bin/env python3 "/Use
** File not found: numbers.txt **
Processed
0 numbers.
Results
written to
results.txt
results.txt
exists.
Found file:
SingleAArma_Lab3_d
Found
file:
results.txt
Found
file:
README.md
Found file:
•git
x bigger
equal
Loop index 0
Loop index 1
Loop index 2
Reached two
Loop index 3
Loop index 4
Counter is 3
Counter is 4
Counter is 5
Counter is 6
Counter is 7
Counter is 8
Counter is 9
Counter is 10
Flawed function result:
2.0
Nested indices
00
Nested indices
0 1
Nested indices
02
Nested
indices
10
Nested
indices
1 1
Nested
indices
12
Flag is
truthy
```
- created `numbers.txt` file via command line - touch numbers.txt *Dont forget to enter this WITHIN the working directory and not one level up or you will have spaghetti night* ....

- next reran the python script and encountered  some more errors but the errors pointed to 
Line 91 in the `index4.html` file. Needed a closing bracket from the previous else if statement on Line 89 . Added { to cure. Included in the index.html section.

- Fixed line 31 logic error. Replaced '0' with len(numbers) to cure.
```
avg = total / len(numbers)
```
- Fixed line 92: Added '-' in place of '+' to cure.

```
counter -= 1
```
THIS HAS CONCLUDED THE PYTHON FILE FIXES

Python file run after some updates in the other files:
```
Processed 4 numbers.
Results written to results.txt
results.txt exists.
Found file: script4.js
Found file: python_app4.py
Found file: numbers.txt
Found file: index4.html
Found file: results.txt
Found file: script4.sh
x bigger
equal
Loop index 0
Loop index 1
Loop index 2
Reached two
Loop index 3
Loop index 4
Counter is 3
Counter is 2
Counter is 1
Counter is 0
Flawed function result: 2.0
Nested indices 0 0
Nested indices 0 1
Nested indices 0 2
Nested indices 1 0
Nested indices 1 1
Nested indices 1 2
Flag is truthy
```
_______
# numbers.txt file 
- Since I created the numbers.txt file based on the not found message, I was looking for the file to populate numbers inside of it ,but it did not, so I added 80,95,75,85 based on the numbers used on the scoreboard. 

- The results.txt file generates a `Total` and `Average` . Im still trying to troubleshoot why the results.txt only generates numbers when the numbers file is outside of the main directory and not inside.  
*Update - Resolved by creating the numbers.txt file within the main working directory*
______

# script4.js file
- ran `node script4.js` command and received output: 
`script4.js:110
Line 110 else { // syntax error: missing closing parenthesis`

- Added closing bracket at line 110 before else statement to cure.
```
} else { // syntax error: ~missing closing parenthesis~
```
- Ran the script4 file again and the following output occured:
```
❯ node script4.js
Average score: 82.5
Highest score: Infinity
Lowest score: -Infinity
Average score: 85
Highest score: Infinity
Lowest score: -Infinity
Average score: 85
Highest score: Infinity
Lowest score: -Infinity
Converted '42' to 42
Sum of scores: 0  "this sum of 0 is actually an error, explained on Line 71"
cnt is 3
cnt is 4
cnt is 5
cnt is 6
cnt is 7
cnt is 8
cnt is 9
cnt is 10
cnt is 11
cnt is 12
cnt is 13
cnt is 14
cnt is 15
cnt is 16
cnt is 17
cnt is 18
cnt is 19
cnt is 20
Good
i: 0 j: 0
i: 0 j: 1
i: 1 j: 0
i: 1 j: 1
i: 2 j: 0
i: 2 j: 1
```
- Highest score and Lowest score seems to not be displaying numerical value. Per Line 100 in the script4.js file, there was an comment stating logical error, increment instead of decrement. Since the cnt entries are counting upward, the script needs to be adjusted to reflect the decrement.
- Fixes: Line 27 `var max = Infinity` needs to be revised to `var max = -Infinity;`
- Line 28 `var min = -Infinity;` needs to be revised to `var min = Infinity;`
```
var max = -Infinity;
var min =  Infinity;
```
- Line 71 had an additional error: if (players.length = 0) need to be updated to a `Strict Equality Comparison` . Without this, the sum of scores will reflect `0` instead of the intended `340` . Updated entry to if (players.length === 0) to cure.
    ```
    if (players.length === 0)
    ```
- After implementing these fixes, current output:
```
Average score: 82.5
Highest score: 95
Lowest score: 70
Average score: 85
Highest score: 95
Lowest score: 75
Average score: 85
Highest score: 95
Lowest score: 75
Converted '42' to 42
Sum of scores: 340
cnt is 3
cnt is 2
cnt is 1
Good
i: 0 j: 0
i: 0 j: 1
i: 1 j: 0
i: 1 j: 1
i: 2 j: 0
i: 2 j: 1
```
________
# script4.sh
- To run the script, command `bash script4.sh` is needed but it needs a file name or else it returns blank. It needs to run with a file name. I used the numbers.txt that I created: `bash script4.sh numbers.txt`
- The following output from running the script4.sh highlighted some errors:
```
❯ bash script4.sh numbers.txt
Lines:        3
Words:        4
Characters:       11
script4.sh: line 24: word_count / 0: division by 0 (error token is "0") - this is actually a logic error.
Average words per line: 
1: 82
2: 95
3: 70
script4.sh: line 76: syntax error near unexpected token `else'
script4.sh: line 76: `    else'
```
- Line 23 logic error noted. avg_words=$((word_count / 0)).
- Line 24 Replaced with  avg_words=$((word_count / line_count))
```
avg_words=$((word_count / line_count))
❯ bash script4.sh numbers.txt
Lines:        3
Words:        4
Characters:       11
Average words per line: 1
1: 82
2: 95
3: 70
script4.sh: line 76: syntax error near unexpected token `else'
script4.sh: line 76: `    else'
```
- Line 34 mentions another syntax error, and there was an opening bracket but missing the closing bracket was missing. Added } on line 44 to cure.
```
        echo $longest
    # Missing closing brace intentionally. # Added closing bracket to cure.-A.D.
} 
```
- Line 65 has logic error, changed increment to decrement
    ```
    counter=$((counter - 1))
    ```
- Line 74 if statement was missing '; then ' Added to cure 
    ```
    if [ -z "$str" ]; then
    ```

After the corrections, here is the output from script4.sh :
```
Words:        4
Characters:       11
Average words per line: 1
1: 82
2: 95
3: 70
Longest word: 82
Total words counted in loop: 4
i=0 j=0
i=0 j=1
i=1 j=0
i=1 j=1
i=2 j=0
i=2 j=1
Counter 3
Counter 2
Counter 1
String is empty
String is not empty
```
___________

# index4.html troubleshooting
- This required me to add the `Live Server` extension in vscode to view the Game Scoreboard and debug console. Here is the output that presented as soon as I opened the console:

```
    Uncaught TypeError: can't access property "children", rows[i] is undefined

    calculateScores http://127.0.0.1:5500/SingleAArma_Lab3_d/index4.html:33  

    displaySummary http://127.0.0.1:5500/SingleAArma_Lab3_d/index4.html:48  

    onload http://127.0.0.1:5500/SingleAArma_Lab3_d/index4.html:57  

    EventHandlerNonNull* http://127.0.0.1:5500/SingleAArma_Lab3_d/index4.html:56
```
- Line 32 of index4.html displays a logic error:  `<= leads to undefined` . Removed '=' to cure.
    ```
    for (var i = 0; i < rows.length; i++)
    ```
- This clears out the all  errors except for  previously listed `404 Not Found error` which seems to be hardcoded.

- Lines 42 and 43 contain logic errors, wherein `min` and `max` where imputed incorrectly. Swapped min and max on each respectively to cure. 
- This resolved misrepresented data on the webpage wherein Highest was displayed as 70 and lowest 95.
    ```
    var max = Math.max.apply(null, scores);
    var min = Math.min.apply(null, scores);
    ```
- Line 82 displays a logic error again where max and min needs to be switched respectively:
    ```
    return { average: avg, max: Math.max.apply(null, arr), min: Math.min.apply(null, arr) };
    ```
- Line 91 synax error which was briefly mentioned in troubleshooting the `python_app4.py` file. Resolved by placing the closing bracket carried over from the `else if ` statement before else:
```
    } else if (score < 50) {

console.log("Lose");

    } else { 
```   
- Line 106 contains logic error `index++`;. Replaced increments '++' with correct decrement '--' to cure:
```
    var index = 5;

while (index > 0) {

index--; // logic error: increments instead of decrements.

if (index > 20) break;

}
```

# *This concludes the debugging lab*
