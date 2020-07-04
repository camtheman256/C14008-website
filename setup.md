@def title="Getting Setup for C14008"
@def maxtoclevel=2

# Getting Setup with Julia for C14008

In C14008, you will receive [Jupyter](https://jupyter.org/) notebooks every week containing much of the course content for that week, along with some exercises and extracurricular activities that you're welcome to undertake to learn more about the Julia language.

@@colbox-blue
  **Need help with this guide?** Email [c14008-teachers@esp.mit.edu](mailto:c14008-teachers@esp.mit.edu) and we'll come help you out.
@@

There's a couple ways we will be enabling you to work with Julia.

\toc

### Deciding between local development and the code server
You may want to [develop on your own machine](#installing_julia_on_your_computer) if you:
- are running MacOS, Windows, or Linux
- are comfortable installing development tools on your own machine
- have a powerful enough computer to run Zoom and whatever program you choose to edit Julia with at the same time

You may want to [use the code server](#using_the_course-provided_code_server) if you:
- have an older or less powerful computer
- are using a device without administrator permissions or a device you don't own
- are using a Chromebook, iPad, or other device that doesn't run MacOS, Windows, or Linux
- are less comfortable installing software on your computer

## Installing Julia on your computer

### Setting up Jupyter
Make sure you have Python installed on your computer, which you will need to use Jupyter.

@@colbox-blue
  **Differences between Jupyter and JupyterLab:**
  Jupyter features the essential notebook programming environment with a simple file browser, while [JupyterLab](https://jupyterlab.readthedocs.io/en/stable/index.html) is more like an [IDE](https://en.wikipedia.org/wiki/Integrated_development_environment) such as Eclipse or IntelliJ.

  To see what JupyterLab is like before installing, visit the code server (which runs JupyterLab!) by following the instructions under [Using the course-provided code server](#using_the_course-provided_code_server).

  If you don't know which notebook environment to use, we recommend JupyterLab.
@@

#### Easy way: installing Anaconda
Anaconda is a distribution of Python that bundles a lot of tools that are helpful for data science, including Jupyter and JupyterLab. To install Anaconda, visit [the download page](https://www.anaconda.com/products/individual).

Follow the instructions to install Anaconda, then launch Anaconda and use the graphical interface to download Jupyter or JupyterLab. Now, skip ahead to [Setting up Julia](#setting_up_julia).

#### Lightweight way: installing Python manually
 Mac, Windows, and Linux users can install Python by visiting the [downloads page](https://www.python.org/downloads/). Ubuntu and Debian users can install Python 3.8 with the following command:[^1]
 ```bash
 $ sudo apt install python3.8
 ```

Now, to install Jupyter or JupyterLab, follow [the instructions](https://jupyter.org/install) on the Jupyter Website.

[^1]: Other Linux distributions, such as Arch and Fedora, likely have packages to install Python 3.8 in their central repositories. You may need to research the correct command to run.

### Setting up Julia

@@colbox-blue
C14008 requires **Julia 1.4**.
@@

#### Easy way: installing JuliaPro
Like Anaconda, [JuliaPro](https://juliacomputing.com/products/juliapro) is a distribution of Julia that bundles many Julia packages that are useful for development and data science. To install JuliaPro, use the installers on [the download page](https://juliacomputing.com/products/juliapro#download-table).

#### Lightweight way: installing Julia manually
Julia can be installed manually by using [the installers on the Julia website](https://julialang.org/downloads/). Ubuntu 20.04 and possibly some Debian users may be able to install Julia with the following command:
```bash
$ sudo apt install julia
```

To install IJulia, which makes Julia work with Jupyter notebooks, launch the Julia REPL (potentially by running `julia` in your command line) and run:
```julia-repl
julia> using Pkg; Pkg.add("IJulia")
```

You're welcome to use any editor you like and run Julia from the command line, but if you've installed manually, we encourage you to take a look at [Juno IDE for Julia](https://junolab.org/). It's what comes with JuliaPro and it's also what the instructors will be using outside of JupyterLab.

Congratulations! You are set up with Julia for C14008.

## Using the course-provided code server

The code server can be located at [code.julia.party](https://code.julia.party). With the code server, you are provided with a JupyterLab workspace and a space to store your files for the class. You don't have to use it if you'd prefer to use your local machine, but we're going to require everyone to sign up for the server, in case we end up using it for assignments or something.

### Signing up for an account
Visit the [signup form](https://code.julia.party/hub/signup) on the code server. Type in a username and a password you'd like to use for the code server. The code server won't activate your account immediately; instead, it will send your username to us for activation.

In the welcome form, which you should've received by email, **write down the username you used**. This will allow us to tie your code server account to your registration with HSSP. We won't activate accounts that aren't attached to actual users.

We'll attempt to activate your account within 12 hours of you requesting access. However, there won't be any notification that your account is activated.

### More information on the code server
Visit [this guide](/code-server) for more information on how to use the code server. Once your account is approved and you've filled out the welcome form, you're welcome to hack and code away on the code server at your discretion, regardless of whether you said on the form you would be needing it or not.
