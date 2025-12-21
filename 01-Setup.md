You need two(2) things to start programming in C;

1. An environment where you can write your C programs `etc` A Text editor or IDE (Integrated Development Environment) for this course, we use `codeblocks`.

2. A compiler - Should incase you downloaded just a `text-editor`, you would need a `compiler`

# Windows Setup
- Search for `codeblocks` in your browser.
- Click on downloads.
- Click the binary release and select for your system architecture.
- Go for the `codeblocks` with `mingw` setup, what this does or means is that we can install the IDE (`codeblocks` and also a C compiler).
- And click `sourceforge` to get you the file.


> [!NOTE] 
>  Install the program
> 
>  Leave the installed setup as default
> 
> set/select the `gnu gcc compiler` to set as default or the one highlighted.

Earlier on when run this command in our command prompt to check the version of C running, we got nothing;

```c
gcc --version
```
If you do have IDE already and want to install the compiler, take note of the installation path of this `C:\Program Files\CodeBlocks\MinGW\bin`. Copy it, search for environment variables in your windows and edit path. Add new by selecting new and paste that path with `bin` should install in a different directory, that's the path to the compiler.

# Mac Setup

1. Go to your terminal: check if you have C installed.

```command
cc -v
```

To install:

```command
xcode-select --install
```

2. Download the `codeblocks` IDE.
- Click on downloads.
- Click the binary release.
- Scroll down to Mac and download.
