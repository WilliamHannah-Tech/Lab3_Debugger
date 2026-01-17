# SingleA_Armageddon_VersionD
collection of code files for troubleshooting exercise and practice. Time to git ghud, padawans.

# Debugging Errors & Actions
                                #index4.html
1. "Uncaught type error" :Cannot read properties of undefined (reading 'children')
 @ at calculateScores (index4.html:33:37) line#33 runtime error resolution: 
    at displaySummary (index4.html:48:25) Resolution:
    at window.onload (index4.html:57:13) Resolution:
2. Failed to load resource: the server responded with a status of 404 (Not Found)Understand this error
3. Runtime TypeError: (line#32) Delete the (= sign)
4. Runtime error: (line#56) Had to addEventListener
5. Logical Error: (line#82) Reversed the "min" & "max" functions
6. Logic Error: (Line#106) Changed increment "++" to a decrement "--"
7. Logic Error: (Line#42 &43) Min & max variable were swapped 
   
                                #Python_app4.py

1. Logical Error: (Line#16) Use "Float" to support decimals and whole numbers
2. Runtime Error: Zero-Division-Error (Line#31)  Replace "0" with the "len(numbers)" function
3. Syntax Error: (Line#85) Added a ":" after (else keyword) :Every python stmnt must end with a ":"
4. Ifinite Loop/ Logic error: (Line#92) Changed the "counter "+" to a "-" to flow towards the exit condition
5. Syntax Error: (Line#97) The flawed_function header (def) must end with a "colon" 
   
                                #script4.js
1. syntax error: "else statement trapped inside "else block" (line#109) place closing brace before last "else"
2. logic error: "should initialize to -infinity & infinity" (line#26-27) swap the "-" sign on the infinity variable
3. Dependincie error: "Additional code with errors" (line#57) Looped backwards to Remove additional items
4. Syntax error: "Intentional syntax error in comparison" (line#70) Used the strict equality operator (===) to check value 
5. Runtime error: NAN "Not A Number" (LIne#75-76) Put a "10" in the string
6. Logic error & loop: "Long condition leads to no iteration" (Line#91) Change condtion to k >= 0
7. Logic error & Loop: "Loop demostrating incorrect update" (Line#96-100) Decrement the Variable
8. "Additional filler loops for line count" 

                                #Script4.sh

1. Runtime Error: (Line#24) Use the "line_count" variable to make sure I dont divide by Zero
2. Syntax Errors: (Lines#37,38,38) Quotes were needed to prevent empty vairables & closing brace applied
3. Infinite Loop & Logic Error: (Line#65) Decrement apllied (+) to (-) so counter moves to 0
4. Syntax Error: (Line#74) Semicolon was needed at the end of "if" Bash function