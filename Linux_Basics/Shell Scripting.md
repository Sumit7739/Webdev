### Shell Scripting

Shell scripting in Linux allows you to automate tasks, making system administration more efficient. By writing scripts, you can sequence commands, manage system operations, and create custom utilities tailored to your needs.

#### 1. **Writing and Executing Shell Scripts**

- **Creating a Script**:
  - **Shebang**: Start your script with a shebang (`#!`) to define the shell interpreter. The most common shebang for Linux scripts is `#!/bin/bash`, which specifies the Bash shell.
  - **Script File**: Write your commands in a plain text file and save it with a `.sh` extension.

  - **Example**:
    ```bash
    #!/bin/bash
    echo "This is a basic shell script."
    ```

- **Making the Script Executable**:
  - Before you can run your script, you need to make it executable using the `chmod` command:
    ```bash
    chmod +x script.sh
    ```

- **Running the Script**:
  - Execute the script from the terminal:
    ```bash
    ./script.sh
    ```

#### 2. **Basic Scripting Concepts**

- **Variables**:
  - **Purpose**: Variables store data that your script can use and manipulate.
  - **Declaration**: Assign values without spaces around the `=` sign.
  - **Accessing Variables**: Use `$` before the variable name to access its value.
  - **Example**:
    ```bash
    name="Sumit"
    echo "Hello, $name"
    ```
  - **Best Practice**: Use double quotes around variables to prevent issues with spaces in values.

- **Loops**:
  - **Purpose**: Loops allow you to execute a block of code repeatedly.
  - **Types**: 
    - `for`: Iterates over a list of items.
    - `while`: Repeats as long as a condition is true.
    - `until`: Repeats until a condition becomes true.
  - **For Loop Example**:
    ```bash
    for i in {1..5}; do
      echo "Loop iteration: $i"
    done
    ```
  - **While Loop Example**:
    ```bash
    counter=1
    while [ $counter -le 5 ]; do
      echo "Counter: $counter"
      ((counter++))
    done
    ```

- **Conditionals**:
  - **Purpose**: Conditionals let you make decisions in your script.
  - **Syntax**: The `if [ condition ]; then ... fi` structure is used to execute commands based on conditions.
  - **Example**:
    ```bash
    if [ "$name" == "Sumit" ]; then
      echo "Welcome, Sumit!"
    else
      echo "You are not Sumit."
    fi
    ```
  - **Advanced Usage**: Combine multiple conditions using `&&` (and) or `||` (or).

- **Functions**:
  - **Purpose**: Functions encapsulate a block of code that you can call multiple times within your script.
  - **Declaration**: Functions are defined with a name followed by `()` and enclosed in `{}`.
  - **Example**:
    ```bash
    greet() {
      echo "Hello, $1!"
    }
    greet "Sumit"
    ```
  - **Arguments**: Functions can take arguments, accessed using `$1`, `$2`, etc.

- **Best Practices**:
  - **Commenting**: Use comments (`#`) to describe what your script or specific sections do.
  - **Error Handling**: Incorporate checks and error handling to make scripts robust.
  - **Testing**: Test scripts in a safe environment before deploying them in production.

By understanding these scripting basics, you can automate complex tasks, making your work on Linux systems more streamlined and powerful.

Go back to topics page [[Linux Basics]].