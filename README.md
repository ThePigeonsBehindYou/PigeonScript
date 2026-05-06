# PigeonScript

Monorepo for PigeonScript

## Usage

PigeonScript uses opcodes and operands separated by spaces, with instructions separated by newlines (`\n` is different to `\r\n`).

Opcodes:

- `add` adds or joins two operands together.
- `sub` subtracts two operands from each other. If either is a string, it will remove the first occurance of the second operand from the first using RegEx.
- `gsub` is like `sub`, except it removes all occurances of the second operand.
- `mul` multiplies two operands together. If either is a string with one being a number, the string will be repeated by the other operand, otherwise if they are both strings they will be joined.
- `div` divides the first operand by the second operand. If either is a string, it returns NaN.
- `pow` raises the first operand to the second operand. If either is a string, it returns NaN.
- `root` takes the first operand-root of the second operand. If either is a string, it returns NaN.
- `neg` negates the first operand. If it is a string, it reverses it instead.
- `sign` gives you the sign of the provided number.
- `clamp` clamps the first number between the second and third numbers as bounds.
- `test` tests for a condition in the format `op1 operator (op2)`, where the operators are `!=`, `=`/`==`, `<`, `>`, `<=`, `>=`, `mul` (is op1 a multiple of op2?), `safe` (is op1 a safe number?), `num` (is op1 a number?), `int`, and `float`.
- `goto` changes the program counter to that line (the counter starts at 1).
- `gotoif` is a conditional goto; it tests for a condition using the `test` command. If it succeeds, jump to the program counter (provided as the last argument).
- `write` writes the text on the screen. If the number of lines exceeds the possible amount, it clears.
- `import` runs the provided script without the file extension.
- `sleep` sleeps for that amount of seconds.
- `set` sets the variable named by the first operand to the second operand.
- `playsound` plays the sound given from the URL until done.
- `startsound` starts the sound given from the URL.

To use variables in instructions, use `$VARIABLE_NAME`. It will only work at the start of an opcode as PigeonScript only parses the beginning of the opcode and not the middle or end. The results of operations will be stored in `$RESULT`.

### On OSes

To use it on an OS, create an archive named `PigeonScript` with the main script inside called `main.ps`. Then broadcast the `pigeonscript:execute` broadcast. Exiting PigeonScript mode is possible through backspace, which also halts the current execution.

### Demo

To demo PigeonScript, you can do so at [this page](https://thepigeonsbehindyou.github.io/PigeonScript/PigeonScript-demo.html). Current demo version: `v0.1.0a`

## Release Cycle

Full releases will not have any suffix, while prereleases will have suffixes such as α, β, γ, and δ. The first number denotes major release, the second denotes minor release, and the third denotes the hotfix/patch.
