@def title="Setting up Julia FAQ"

# Setting up Julia FAQ

This page contains some notes on the installation process to help explain some of the various tools you'll be using. See below for some frequently asked questions and notes.

\toc

## What is the Juno IDE and how is it related to Atom text editor?
The [Juno IDE](https://junolab.org/) installed by JuliaPro _is_ actually a text editor called [Atom](https://atom.io) with some plugins, most notably the [uber-juno](https://atom.io/packages/uber-juno) package installed. However, note that if you have Atom installed when you install JuliaPro, **instaling Juno IDE will replace your current installation of Atom.** Also, uninstalling JuliaPro will likely uninstall JuliaPro's bundled Atom, so you will need to reinstall Atom again after uninstalling JuliaPro.

JuliaPro installs a number of Julia-related plugins on top of your current Atom configuration. The Julia plugins won't prohibit you from working on non-Julia files in Atom, though if you want them out of your way, you can disable the [julia-client](https://atom.io/packages/julia-client) package.

## Why can't I run `julia` from Command Prompt/Powershell after installing with JuliaPro? (Windows)
JuliaPro, annoyingly, doesn't add Julia to your PATH, which is a list of directories that your command line looks through to find the command you want to run. If you want to access the Julia REPL and run Julia code, you can use Juno IDE. If you would like to do so from your command line, follow these instructions to add julia.exe to your path:
1. From the start menu, run "Edit the system environment variables"
2. Click the button that says "Environment variables..."
3. Under "User variables for [username]", double click on Path
4. Click "New" in the pop up
5. Add your Julia bin directory:[^1]
    - If you installed for the current user (which is the default), type in `%USERPROFILE%\AppData\Local\JuliaPro-1.4.2-1\Julia-1.4.2\bin`
      - If you're wondering, the `%USERPROFILE%` variable just points to your user directory.
    - If you installed system-wide (by running JuliaPro with administrator permissions), type in `C:\JuliaPro-1.4.2-1\Julia-1.4.2\bin`
  
[^1]: These instructions are assuming you've installed JuliaPro 1.4.2-1, which is the current version as of this writing. If you're running a different version of JuliaPro, adjust the version numbers in the file paths.
