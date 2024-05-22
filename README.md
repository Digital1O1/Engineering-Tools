# Reference chart
# GDB Commands Cheat Sheet

| **Action**                        | **Command**                                         | **Description**                                                 |
|-----------------------------------|-----------------------------------------------------|-----------------------------------------------------------------|
| **Run GDB**                       | `gdb ./main`                                        | Runs the debugger                                               |
| **Step Into**                     | `step` or `s`                                       | Step into the next function call.                               |
| **Refresh**                       | `refresh` or `ref`                                  | Refreshes terminal                                              |
| **Step Over**                     | `next` or `n`                                       | Execute the next line of code, stepping over function calls.    |
| **Step Out**                      | `finish`                                            | Continue running until the current function returns.            |
| **Set Breakpoint**                | `break filename:line_number`                        | Set a breakpoint at a specific line.                            |
|                                   | `break function_name`                               | Set a breakpoint at a specific function.                        |
| **List Breakpoints**              | `info breakpoints`                                  | List all breakpoints.                                           |
| **Delete Breakpoint**             | `delete breakpoint_number`                          | Delete a specific breakpoint.                                   |
| **Run Program**                   | `run`                                               | Run the program.                                                |
| **Continue Execution**            | `continue`                                          | Continue execution until the next breakpoint.                   |
| **Print Variable**                | `print variable_name`                               | Print the value of a variable.                                  |
| **Print Variable (Hexadecimal)**  | `print /x variable_name`                            | Print the value of a variable in hexadecimal format.            |
| **Display Call Stack**            | `backtrace`                                         | Display the call stack.                                         |
| **Display Detailed Call Stack**   | `backtrace full`                                    | Display detailed information in the call stack.                 |
| **Examine Memory**                | `x address`                                         | Examine memory at a specific address.                           |
| **Examine Memory (Hexadecimal)**  | `x/x address`                                       | Examine memory in hexadecimal format.                           |
| **Examine Memory (String)**       | `x/s address`                                       | Examine memory as a string.                                     |
| **Set Watchpoint**                | `watch variable_name`                               | Set a watchpoint to stop execution when a variable changes.     |
| **List Watchpoints**              | `info watchpoints`                                  | List all watchpoints.                                           |
| **Select Frame**                  | `frame frame_number`                                | Select a specific frame in the call stack.                      |
| **Move Up Call Stack**            | `up`                                                | Move up the call stack.                                         |
| **Move Down Call Stack**          | `down`                                              | Move down the call stack.                                       |
| **Quit GDB**                      | `quit`                                              | Exit GDB.                                                       |
| **Restart Program**               | `run`                                               | Restart the program from the beginning.                         |
| **Restart with Arguments**        | `run arg1 arg2`                                     | Restart the program with specific arguments.                    |
| **Source Code View**              | `layout src`                                        | Switch to the source code view.                                 |
| **Assembly Code View**            | `layout asm`                                        | Switch to the assembly code view.                               |
| **Split Code View**               | `layout split`                                      | Switch to a split view with both source and assembly.           |

## Example Debugging Session

```bash
$ gdb ./my_program
(gdb) break main              # Set a breakpoint at the beginning of main
(gdb) run                     # Run the program
(gdb) next                    # Step over to the next line
(gdb) step                    # Step into a function call
(gdb) print my_variable       # Print the value of a variable
(gdb) continue                # Continue execution until the next breakpoint
(gdb) backtrace               # Show the call stack
(gdb) finish                  # Finish the current function
(gdb) quit                    # Exit GDB
```
# Restarting GDB Session
```bash
$ gdb ./my_program
(gdb) run                     # Start the program
# Program is running...
# Press Ctrl+C to interrupt
(gdb) run                     # Restart the program
(gdb) run arg1 arg2           # Restart with arguments
```


# Switching Views in GDB
```bash
(gdb) layout src              # Switch to the source code view
(gdb) layout asm              # Switch to the assembly code view
(gdb) layout split            # Switch to a split view with both source and assembly
```
