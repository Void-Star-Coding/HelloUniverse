Symbolic Link
  Representations of a file and folder in a different location that
  can be used by applications as if it were in that location.
  
  Soft Links
    Redirect the application to the data
    
  Hard Links
    Trick Windows and the application into thinking the data exists exactly at this location
    
  How to
    Open (elevated) Command Prompt (NOT POWERSHELL)
      Quotation may be placed around the names for spaces or long file paths
      Soft Link to File
        > mklink Location\SoftLinkFileName Location\OriginalFileName.ext
      
      Soft Link to Directory
        > mklink /D NewLocation\SoftLinkFolderName OldLocation\OriginalFolderName
        
      Hard Link to File
        > mklink /H NewLocation\HardLinkFileName.ext OldLocation\OriginalFileName.ext
        
      Hard Link to Folder, aka Junction
        > mklink /J NewLocation\HardLinkFolderName OldLocation\OriginalFolderName
        
  Example:
  
    > mklink aSoftLinkFile OriginalFile.txt
    > mklink /H aHardLinkFile.txt OriginalFile.txt
    > mklink /D aSoftLinkFolder OriginalFolder
    > mklink /J aHardLinkFolder OriginalFolder
    
    Notice Hardlink file appears as if it were a real file, 
    while the Hardlink folder looks like a link until you check its properties.
  
  Usages:
    For quick and dirty code library management and development across multiple projects, 
    you can often Hard Link directories inside the working folders.
    
  Notes:
    Some linked files cannot be uploaded to Github