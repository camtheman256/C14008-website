@def title="Using the Code Server"

# Using the C14008 Code Server

If you don't yet have an account on the Code Server, please follow [the instructions in the setup guide](/setup#signing_up_for_an_account).

Topics:
\toc

## Personal workspace
Logging into the Code Server will immediately launch you into a personal JupyterLab instance for you to use. Your files will persist when you log in and out, and you also have limited terminal access. Use the icons provided in the Launch tab to create a Julia console or Julia notebook for you to work with.

## Resetting your password
If you ever need to change your password, visit [this link](https://code.julia.party/hub/change-password) after you've logged in. If you're locked out of the code server, just email [c14008-teachers@esp.mit.edu](mailto:c14008-teachers@esp.mit.edu), and we'll help you regain access to your account.

## Editing a Julia file on the Code Server
To write Julia on the server, you're welcome to write code in notebooks, but you can also write Julia (.jl) files by creating a text file in the launcher and renaming it to `<filename>.jl`. JupyterLab will automatically recognize you are editing a Julia file and add appropriate syntax highlighting.

### Running a Julia file
To run a Julia (.jl) file, you'll need to open a terminal from the launcher and type `julia <filename>.jl`.

Unfortunately, without using the Juno IDE in a local development environment, you'll have to debug using tactical print statements. You're always welcome to email the instructors for code help, and we can visit your code on the code server.

## Using the Julia REPL
To launch the Julia [REPL](https://en.wikipedia.org/wiki/Read_Eval_Print_Loop), you can open a terminal and type `julia`. From there, you can install and use packages as you normally would, and you can evaluate Julia statements as in the console view. The Julia REPL is a bit like the JupyterLab-provided console tab.

## Using Packages on the Code Server
Packages on the code server are installed for you into a global environment. If you'd like a package that isn't currently installed, just email us at [c14008-teachers@esp.mit.edu](mailto:c14008-teachers@esp.mit.edu), and we'll install it for you.

Occasionally, you may receive this error on the code server if you're trying to use a globally registered package that you haven't loaded in personally yet.
```julia-repl
julia> using Primes
ArgumentError: Package Primes [27ebfcd6-29c5-5fa9-bf4b-fb8fc14df3ae] is required but does not seem to be installed:
 - Run `Pkg.instantiate()` to install all recorded dependencies.
```

To fix this issue, run the following command anywhere you can run Julia. This command will install the package for your personal use.
```julia
using Pkg; Pkg.instantiate()
```
