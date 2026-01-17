Lab 3 Log of errors and fixes

index4.html 

1. // logic error: <= leads to undefined
On line 32: changed code to: for (var i = 0; i < rows.length; i++) 

2. // logic error: min used instead of max
On line 42: changed code to: var max = Math.max.apply(null, scores);

3. // logic error: max used instead of min
On line 43: changed code to: var min = Math.min.apply(null, scores); 

4. // Logic error: returns wrong property names
On line 82: changed code to return { average: avg, max: Math.max.apply(null, arr), min: Math.min.apply(null, arr) };

 5. // syntax error: missing closing parenthesis
On line 91: added a closing parenthesis

 6. // logic error: increments instead of decrements
 On line 106: changed line to index--;



 phython_app4.py

 1. On line 16: Changed int(stripped) to float(stripped)
 2. On line 31: Changed total / 0    to    total / len(numbers)
 3. On line 85: added colon after else
 4. On line 92: changed += 1 to -= 1 to stop the loop
 5. On line 97: added a colon after (x, y)




script4.js

1. On line 26: changed var max = Infinity  var max = -Infinity
2. On line 27: changed var min = -Infinity to var max = Infinity
3. On line 54: added closing brace
4. on line 70: changed if (players.length = 0) to if (players.length === 0)
5. On line 91: change (var k = players.length; k < 0; k--) to (var k = players.length - 1; k >= 0; k--)
6. On line 99: changed cnt++; to cnt--; so it will decrease
7. On line 109: added a closing brace 
8. On line 114: removed extra closing brace 


script4.sh

1. On line 24: changed avg_words=$((word_count / 0)) to avg_words=$((word_count / line_count)) because dividing by zero will cause a error
2. On line 43: added a closing brace
3. on line 65: changed + 1 to -1 so itthe counter will decrease
4. On line 74: chaneged if [ -z "$str" ] to if [ -z "$str" ];then
 











