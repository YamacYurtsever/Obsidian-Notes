- Command line interfaces are text-based interfaces used to interact with a computer or software through entering commands into a terminal or console

#### Unix-Based Shell Terms
- **ls** -> List the files in a directory
- **mv** -> Move (Could be used for renaming as well)
- **cd** -> Change directory
- **cp** -> Copy
- **mkdir** Make directory
- **rm** -> Remove file
- **rm -r** -> Remove folder
- **pwd** -> Tell current directory
- **.** -> Current directory
- **..** -> Previous directory
! cd not followed by anything changes the directory to the root

#### Command Line Argument
An additional word or phrase typed after a command in the CLI that modifies the behavior of that command
- [[Parameters]] that are passed to a program or script when it is run from the [[CLI]]
- They allow users to provide input to a program at the time of execution, influencing its behavior
```C
int main(int argc, char *argv[]) {
    // argc: Number of command line arguments
    // argv: Array of strings containing the arguments

    // Accessing arguments
    for (int i = 0; i < argc; i++) {
        printf("Argument %d: %s\n", i, argv[i]);
    }

    return 0;
}
```
! The first argument is always the name of the program
