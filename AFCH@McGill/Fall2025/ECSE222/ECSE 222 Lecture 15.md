# Decoders
Takes in a binary number, and activates the corresponding decimally numbered pin exclusively
Question will typically specify if decoders must have an enable pin
Can be used to represent truth table
# Encoders
Opposite of decoders
$2^n$ input pins $n$ outputs
Outputs binary address of activated input pin
No enable pin

## Example: 4->2 Encoder
Many unused inputs
All unused inputs set to `don't care`
Only inputs that we do care about are those with *exactly* one input bit 1
Truth table:

| w3  | w2    | w1     | w0  | **y1**      | **y0**      |
| --- | ----- | ------ | --- | ----------- | ----------- |
| 0   | 0     | 0      | 1   | **0**       | **0**       |
| 0   | 0     | 1      | 0   | **0**       | **1**       |
| 0   | 1     | 0      | 0   | **1**       | **0**       |
| 1   | 0     | 0      | 0   | **1**       | **1**       |
| Any | Other | Inputs |     | $\emptyset$ | $\emptyset$ |

# Code Converters
# Unsigned Number Multiplication