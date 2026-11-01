# EloPascal — User Guide

EloPascal is a place to write Pascal programs, run them, and see how they work. Use **Run & March** to run a program, or use **Debug Step** to follow it a step at a time and study the values of its variables.

## Your first program

1. Open EloPascal and click inside the code editor.
2. Select all the sample code and replace it with this program:

   ```pascal
   program Hello;
   begin
     writeln('Hello, world!');
   end.
   ```

3. Click **Run & March**. You should see `Hello, world!` in the **CRT Terminal**.
4. Change the message and run the program again.

## Follow a program step by step

Click **Debug Step** to begin debugging. Click it again to advance through the program and observe what happens. You can also focus the code editor and press **Shift+Tab** to start or advance the debugger. Press **Run & March** when you want to run the program normally.

The **Manual Processing (Auto Trace)** table shows program output and variable values as execution progresses. Select **Memory Watch** to inspect variables, including their types and current values. This is useful for checking loop counters and finding where a result changes unexpectedly.

### Example: watch a total grow

```pascal
program RunningTotal;
var
  number, total: integer;
begin
  total := 0;
  for number := 1 to 5 do
  begin
    total := total + number;
    writeln('Number: ', number, '  Total: ', total);
  end;
  writeln('Final total: ', total);
end.
```

Try this with **Debug Step** and watch `number` and `total` in the trace or Memory Watch. Before each step, predict their next values; then compare your prediction with the table.

## Enter input with `read` and `readln`

When a program pauses for input, use the input box in **Manual Processing**: type a value and press **Enter** (or click the Enter button). You do not need to open the CRT Terminal to type input.

```pascal
program Greeting;
var
  name: string;
begin
  write('What is your name? ');
  readln(name);
  writeln('Hello, ', name, '!');
end.
```

Run the program, enter a name in the input box, and watch the greeting appear. You can also use `read` when your program needs input without ending the current line.

## Choose how quickly code runs

Open the **March Speed** list and choose a preset:

- **Instant (Turbo)** runs without animation.
- The animated and slow-walk options make execution easier to follow.
- The deep-trace options slow execution further for studying.
- Choose the custom option to enter a delay in milliseconds per line, from **0 to 2,000**, then apply it.

## Use the editor and panels

Open **Menu** for common file and editor actions:

- **New** starts a blank Pascal file.
- **Open .pas** opens a Pascal file from your device.
- **Format** automatically indents the code.
- **Copy** copies the code; **Clear Code** empties the editor.
- **program.pas** downloads your source code so you can keep or share it.

Use the **CRT Terminal** and **Manual** controls to show or hide those panels. The Manual Processing panel also has buttons to expand the trace, reset it, or download it as Excel or PDF. If a panel is minimized, restore it with its panel controls.

## Keyboard shortcut

| Shortcut | What it does |
| --- | --- |
| **Ctrl+Enter** | Run the program |
| **Shift+Tab** (while the code editor is focused) | Start or advance debugging |

## Tips for learning Pascal

- Start with a small program and add one change at a time.
- Remember that Pascal statements usually end with a semicolon (`;`), and a program usually ends with `end.`
- Use `writeln` to display intermediate values while learning.
- Step through loops and conditions, and predict variable values before advancing.
- If the app reports an error, check the indicated line for a missing semicolon, misspelled name, or unmatched `begin`/`end`.
- The trace is an aid for understanding execution; it does not replace checking your program's logic.

EloPascal is created by **elorabi_abderrahmane** at **esi_alger** to help make learning Pascal more interactive. Thank you for reading and learning with EloPascal—keep experimenting, use the trace to understand what your code is doing, and enjoy building your next program!
