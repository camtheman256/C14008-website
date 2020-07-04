@def title="Using the Code Server"

# Using the C14008 Code Server

If you don't yet have an account on the Code Server, please follow [the instructions in the setup guide](/setup#signing_up_for_an_account).

## Personal workspace
Logging into the Code Server will immediately launch you into a personal JupyterLab instance for you to use. Your files will persist when you log in and out, and you also have limited terminal access. Use the icons provided in the Launch tab to create a Julia console or Julia notebook for you to work with.

## Editing a Julia file on the Code Server
To write Julia on the server, you're welcome to write code in notebooks, but you can also write Julia (.jl) files by creating a text file in the launcher and renaming it to `<filename>.jl`. JupyterLab will automatically recognize you are editing a Julia file and add appropriate syntax highlighting.

### Running a Julia file
To run a Julia (.jl) file, you'll need to open a terminal from the launcher and type `julia <filename>.jl`.

Unfortunately, without using the Juno IDE in a local development environment, you'll have to debug using tactical print statements. You're always welcome to email the instructors for code help, and we can visit your code on the code server.

## Using the Julia REPL
To launch the Julia [REPL](https://en.wikipedia.org/wiki/Read_Eval_Print_Loop), you can open a terminal and type `julia`. From there, you can install and use packages as you normally would, and you can evaluate Julia statements as in the console view. The Julia REPL is a bit like the JupyterLab-provided console tab.
