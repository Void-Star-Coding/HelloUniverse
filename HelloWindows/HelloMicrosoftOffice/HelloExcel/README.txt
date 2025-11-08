Microsoft Excel Pt. 1
  A spreadsheet program that allows calculation, organization, and formatting.
  Be wary of its autofill, especially dates.
  
  On Launch
    Left Panel
      Home (Default)
      New spreadsheet
      Open spreadsheet
      Account
      More
        Options
          Extremely powerful customization, from the tabs and ribbons to more advanced settings.  Don't forget it exists.
          Notable things include
            Formula creation
            Spellchecking and abbreviation expanding
            Macros
            Add-ins, external code that can be used in Excel to make tasks easier
            
   Useful Functions and Keys
    Zoom Ctrl+MWHEELUP/DOWN
    All the way to the end of the spreadshet Ctrl+<Arrow Key>
    Select All Ctrl+A
    Find Ctrl+F
    Replace Ctrl+H
    Autosum Select, Alt++  (plus sign)
    
  Main Panel
    Window/Quick Access Bar
      Autosave
      Save Ctrl+S
      Save As F12
      Undo Ctrl+Z
      Redo Ctrl+Y
      Name of the spreadsheet (default Book1)
    
    The main panel contains Tabs that show Ribbons and the first spreadsheet (default Sheet1).
    Ribbons contain groups of options which often have a small Launch button in the lower right corner for more.
    
    File
      Returns to the starting page
    
      New
      Open
      Share
      Create a Copy
      Export: most notably for CSV files
      
    Home
      Copy Ctrl+C
        Along with many other functions and hotkeys,
        you may select text inside the cell, the cell, or multiple cells
        to perform an action upon them
      Cut Ctrl+X 
      Paste Ctrl+V
      Special Paste Ctrl+Shift+V
        In addition to right clicking for Special Paste Options, 
        this pastes the raw data INSTEAD of any underlying functions or formatting
      Font and Colors
      Alignment
        Most notably Text wrapping
      Conditional Formatting
        Very useful
        Select cells, then apply the format to color them based off of values
        Custom functions may be used
      Analyze Data
        Extremely powerful
        Effectively allows you to make effective formulas and organization by asking or being suggested human-like questions 
    
    Insert
      Mobile Tables
      Illustrations
      Charts
        Typically you have your data organized as a grid with labels at the top already, then apply the charts
    
    Page Layout
      Themes
      Printing related such as margins and orientation
      
    Formulas
      Organized formulas, you can get any of these formulas in the Select Function (Shift+F3) above the cells
      Lookup and reference are more advanced compared to most formulas
      I'll explain more on formulas later
      
    Data
      Extremely useful
      Turn text, Comma Separated Value files, websites, and even pictures into raw dat
      Update information from external sources such as stocks or geodata
      Sort & Filter, most common use for quick alphabetical sort and occasionally cleaning input
      Mastering this makes data entry much easier
      
    Review
      Editing and Collaboration
      
    View
      Most options don't affect the document, and just help in the Review stage
    
    Developer
      Typically forms, interactions, and occasionally code.
    
    Help
      Find functions, Ribbon options, or get help
  
  Cell Name and Function Bar
    Above the spreadsheet has two/three entry options
    Cell Location
    
    (Accept, Deny and Select Function Shift+F3) and Function bar
      After selecting a cell, the function bar allows you to type in the cell or the function bar.
      To the left of the function bar is DENY and ACCEPT cell changes or Select Function that is then
      written inside the Function Bar.
      
      Functions are one of the most valuable things in Excel.  Functions are used like so
        =function(Cell1, Cell2...)
        
      The equals operator also indicates you want to do something mathematical related to the cell, such as simple arithmatic.
        =A1 + B2
      Will add the two values, and display the end result within the cell.  By default, this automatically updates.
      You can refer to named ranges, which is effectively the text in the name 
      of the top most cell of a column or left most cell in a row!
      
      If you need to use the equal sign without performing an equation, you can type the apostrophe (') before it such as
        '=
     and it will show only the equals sign.
     
  (Current) Spreadsheet
  
  Available Spreadsheets in the file
    Below the Spreadsheet there are tabs that can let you choose, add/remove, and rename the spreadsheets in the file.
 