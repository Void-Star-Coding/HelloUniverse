Command Prompt
  https://learn.microsoft.com/en-us/windows-server/administration/windows-commands/windows-commands
  What is it?
    "Each shell is a software program that provides direct communication between you and the operating system or application, providing an environment to automate IT operations."
    
    A text-input executioner.  Given standard commands, it will output something with them.  
    For the simplest usage, you may type in the console
      > command
    Press Enter to run, information, if any will show up in the next line
    
    Command Prompt (CMD) interprets text input under the Windows Command Prompt shell.
    CMD can allow you to do nearly anything on Windows a program's respective gui can and more.
    Addittionally, One can make files.bat called Batch scripts to execute its script langauge in the CMD shell.
  
  To Access the Command Prompt 
    WIN "CMD"
    shift+rclick in a directory/folder to open console at location
      * If the keycombo does not show Command Prompt
          Option A: Alt+D, type "cmd" into the address bar at the desired location, and press enter
          Option B: Open Powershell, type "cmd", press enter, and the terminal will assume Command Prompt
          Option C: shift+rclick->Open in Terminal option
            - Ctrl+, (yes that's a comma) or Right click the window's bar -> Settings
            - Startup -> Default Profile -> change "Windows Powershell" to "Command Prompt"
            
            + To run Command Prompt as Administrator by default
              . Settings -> Command Prompt (or Defaults if you want all Terminals) -> turn on "Run this profile as Administrator" 
              . This will also restart the current windows as Administrator
              
      * Additionally, if you prefer the old rclick menu
        /!\ WARNING: Editing the registry may have unexpected and even Windows destroying side effects.
        Make sure to "backup" your computer before performing any registry edits...
        In Command Prompt (or Powershell)
          > reg.exe add "HKCU\Software\Classes\CLSID\{86ca1aa0-34aa-4e8b-a509-50c905bae2a2}\InprocServer32" /f /ve
        To undo
          > reg.exe delete “HKCU\Software\Classes\CLSID\{86ca1aa0-34aa-4e8b-a509-50c905bae2a2}\InprocServer32” /f /ve
  
  
  Useful information
    highlight text + rclick to copy
    rclick to paste
    rclick window to change defaults or current properties
    > <command> /? ---- provides info
    
    Adding commands that autorun on terminal open, useful for those pesky popup windows
    /!\ WARNING: Editing the registry may have unexpected and even Windows destroying side effects.
    /!\ Make sure to "backup" your computer before performing any registry edits...
    WIN+R "regedit" -> goto Computer\HKEY_CURRENT_USER\Software\Microsoft\Command Prrocessor
      Add Key String called "Autorun"
      <insert autorun commands here>
    press <tab key> to autocomplete names
  
  
  Useful Basics
    Running executables
    Changing settings
    
  Running Commands and Executables
    When you enter an input, it first parses by looking for standard commands
    Then it looks through the current directory for the executable
    Lastly, it looks in your PATH variable to run
      To add an executable to your PATH
        WIN "Environment Variables" -> Environment Variables -> New
  Operators
    command > filename    redirects the output of a command into file, overwrites
    command >> filename   appends the output to a file, creates
    command < filename    takes input from a file, and sends it to a command
    command1 | command2   pipelines the output of one command into another command, findstr is common
    handle1 >& handle2    writes the output of handle1 to handle 2, default 1
      handles:
        STDIN   0   keyboard input
        STDOUT  1   standard command prompt text output
        STDERR  2   error output to command prompt window
        UNDEF   3-9 application defined
    handle1 <& handle2    reads the input of handle2 and writes it to the output of handle1, default 0
  
  Commands
    https://superuser.com/questions/229945/where-are-the-standard-windows-prompt-commands-files
    
    Common
      help    Lists almost all commands with information
        help command    Additional information about command
      cls     clear screen
      echo    text to be printed, typically used in conjuction with yielding information
        echo[     prints an empty line
        echo(     prints an empty line
        echo.     prints an empty line
      type file.txt   view the contents of a text file
      attrib      shows and changes file attributes, explored in HelloAttrib
      robocopy    robust copy, explored in HelloRobocy
    
    Directory
      cd directoryname    changes to directory (as a path typically from C:\ drive), NOT case sensitive
        cd \              moves to root (typically C:\)
        cd ..             moves up directory
        cd .\             moves to directory relative to current
        cd /d directoryname   changes drive and moves directory
      dir                 lists (current) folder contents
      mkdir foldername    makes directory (folder) at current location/directory/working directory
        mkdir "folder name"   encapsulate folders with spaces or other special characters with quotes
      md foldername       same as mkdir
      ren oldname newname Renames oldname to newname
      copy loc\filename.extension newloc\newname.extension  copies FILES from one loc to another
        copy filename.extension "new file name".extension
      xcopy loc\directoryname newloc\newdirname   copies the folder and files
        xcopy /s /i dir1 dir2   ensures non-empty subdirs are copied and creates a new folder if dest DNE
      robocopy folderfilesrc folderfiledest   Robust copy - 
      del                 deletes files * must be confirmed
        del /h            deletes hidden files
        del *.ext         deletes all files in curdur of type
        del name*.*        deletes all files 
      rd  dirname         Removes Directory
      move loc1 loc2      Moves files and folders to 
      
    Misc
      <Drive Letter>:     changes current drive
        /d                
      
    Post-ops
      command /?  same as using help command
      
    Variables
      %userprofile%   Directory of current user, typically c:\Users\Username
  
    Wildcards & Regex 
      https://learn.microsoft.com/en-us/dotnet/standard/base-types/regular-expression-language-quick-reference
      "A regular expression is a pattern that the regular expression engine attempts to match in input text. A pattern consists of one or more character literals, operators, or constructs."
      
      Regex is used to match text that can then be used in commands.  
      Knowledge of Regex is required in conjuction with Command Prompt skills for achieving mastery.
   
   Environment / PATH Variables 
    

  
Windows Terminal

Powershell