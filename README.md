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
- `goto` changes the program counter to that line (the counter starts at 1).
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

As of v0.1.0b, the demo version has been removed, meaning you can only demo v0.1.0a. It may be readded in a future release.

## Release Cycle

Full releases will not have any suffix, while prereleases will have suffixes such as α, β, γ, and δ. The first number denotes major release, the second denotes minor release, and the third denotes the hotfix/patch.
