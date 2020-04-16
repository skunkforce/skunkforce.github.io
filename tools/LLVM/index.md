# LLVM

Installation on windows:
 - download the latest [here](https://releases.llvm.org/download.html)
 - run the installer
 - you probably want to put it in a patch with no spaces (not program files)
 - you probably don't want to add it to your PATH 

 ### why not add to path?
 Development tools run on the command line, whether your using a GUI or not. Commands on the command line like "clang" or "gcc" are actually executable programs which live somewhere. So how does your terminal know where these "commands" live? Through environment variables, you can list the environment variables in windows by opening a power shell terminal and typing 
 
 ```Get-ChildItem Env:```

you should get a long list of variable names and their values, including a variable named ```Path```. By adding to this variable ```Path``` you can add folders who's contents are considered commands.

So if you don't add LLVM, or more specifically its bin folder, to your path the terminal can't 'see' that it has been installed. If you type in ```clang --version``` it will give you an error. 

In power shell we can type in ```$Env:PATH = "C:\LLVM\bin;$Env:PATH"``` and try ```clang --version``` again, now it works. If we close the powershell and open it again and pring the environment variables again we can see that it has forgotten the change. 

So changing the environment every time you want to use an LLVM tool is probably pretty annoying, on the othr hand now you know how everything works and are able to use multiple version of the same tool. If you have multiple versions of something things can otherwise get weird, its good to know what environment variables are set in any given session. You can make a batch script which sets stuff up and launch vscode or similar from it.