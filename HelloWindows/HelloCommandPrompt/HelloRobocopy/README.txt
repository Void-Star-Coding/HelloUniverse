Robocopy
  Robustly Copies file data from one location to another
  
  Useful Switches ( / )
    MT:threads  allows file transfer multithreading, defau;t 8...2-8 is has possible gains, high numbers are better for low file size but may max out other resources  
    E           copy empty folders
    MIR         mirror, after the initial copy, only copies new and changed files and folders, and removes deleted files and folders
    PURGE       mirrors deletion of files and folders from source, and removes them from the destination
    NOCOPY      copies nothing, useful with purge
    MOV         copies files to destination, then deletes from source
    MOVE        copies files and folders/directories to destination, then deletes them from source
    R:tries     retry copy, default 1 million...change to a low reasonable number
    W:seconds   wait time between retries,     
    a+          adds attributes to copied files
      R readonly
      A archive
      S system
      H hidden
      C compressed
      N not content indexed
      E encrypted
      T temporary
    a-          removes attributes from copied files
      same as a+ with additional:
      O offline
   
  Logging
    ns              no size
    nc              no class
    nfl             no file names
    ndl             no directory names
    np              no progress (current / total)
    log:logname     creates/overwrites logfile
    log+:logname    creates/appends logfile
  
  Standard query
    robocopy %userprofile%\Documents D:\backup\%username%\Documents /MT /MIR  /R:2  /W:10 /NC /NP /LOG+:D:\backup\%username%\roblogs\roblog.txt
  
  Scheduling robocopies
    WIN + "Task Scheduler"
    Trigger -> (some recurring time, daily, weekly, or monthyl)
    Action -> somebackup.bat
    Run at highest priveledge
  
 Troubleshooting
  
  Errors
    ERROR 5 (0x00000005) Copying NTFS Security to Destination File
    ERROR 5 (0x00000005) Copying NTFS Security to Destination Directory
      rclick root folder -> properties -> security -> Edit permissions (btn) -> Add User -> type “everyone” -> check names -> ok (btn) -> [chk] Full control -> ok