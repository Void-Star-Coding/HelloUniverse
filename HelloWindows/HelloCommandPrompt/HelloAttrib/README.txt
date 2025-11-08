CMD > attrib
  attrib is an executable that can change the attributes of files.  
  Attributes determine how the windows system views and haandles the files
  
  Usage
    USe + or - to add or remove attributes
    > attrib +attribute -attribute pathname /switches
    
    The command can be run alone 
  
  Switches
    /s    Apply to curret directory and all subdirectories
    /d    Apply to Folders
    /l    Apply to the Symbolic Link, not the target
  
  Attributes List
    r   readonly
    a   archive, becomes an archive(d) file
    s   system, /!\ Warning: be careful with this
    h   hidden
    o   offline
    x   noscrub, stops the periodic anti-corruption measures the from Resilient File System (ReFS)
    v   integrity, forces metadata checksum to reliably detect corruptions
    p   pinned, makes the sync app download the file contents
    u   unpinned, ??? opposite of pinned, doesn't download the contents via a sync app
    b   SMR Blob, I assume makes the file an SMR Blob
    
    
    