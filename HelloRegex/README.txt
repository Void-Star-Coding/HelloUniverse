Wildcard
  "Wildcard" is a way to search for text.  It's sort of rudimentary Regex, but it is NOT regex.
  One must be aware of what kind of pattern matching technique they're working with.
  It's often used by systems and search engines naturally, while regex may need to be specified.
  Not all systems use the same characters, but they often share the same ideas.
  "Wildcard" is used by default in Windows and Unix systems.
  
  Special Characters
    *     Matches 0 or more characters, ex: E*t will match anything that starts with E and ends with t, such as Et or Elephant
    ?     Matches only one character, ex: E*t will only match any 3 length string that starts with E and ends with t
    !     Negates a pattern, matching a character not within the range, may require ^! in shells that remember history
  Common Patterns
    [A-Z] A range of characters that match to a single character within the set
    [a-z]
    [0-9]
    
  Not all systems support these exactly.
    SQL databases may use % as * and _ as ?
    
Regex
  https://regexone.com/
  Regular Expressions (Regex) is effectively a way to match patterns within strings, which consist of characters
  While Regex may vary slightly across systems, its foundation and value of understanding do not.
  Common uses of it are
    Search and replace
    Parsing input
    Console io
  
  Inner Workings
    https://regex101.com/
    
    Regex is matched via a desired pattern.
    The subroutine that hunts for the pattern will "return"
      strings that match
      strings "attached" to objects (such as with file systems)
      captured groups of strings, where they originally matched the pattern
      the objects of which the string matches too
w
    Special Characters
      .   Wildcard, any single character
      \.  raw period
      \?  raw questionmark
      \d  digit, equivalent to [0-9]
      \D  non-digits, equivalent to [^0-9]
      \n  newline
      \t  tab
      \s  space, any kind including tab and newline, equivalent to [ \t\n]
      \S  non-space, any character that isn't space, tab, or newline, equivalent to [^ \t\n]
      \w  any alphanumeric character, equivalent to [A-Za-z0-9_]
      \W  non-alphanumeric characters, equivalent to [^A-Za-z0-9_]
      \b  zero-width word boundary, matches between a word character (\w), and non-word character (\W), as well as the start/end of the string if the first/last charcters in the string are word cahracters...
            ex: .\b matches c in abc
      \B  zero-width non-word boundary, matches the postion between two word charcters between (\w\w) and the position between two non-word characters (\W\W)
            ex: \B.\B matches b in abc

    Quantifiers      
      ?         optionality, the preceeding character or pattern is not necessary
          .?      0 or 1 of any character
      *         0 or more possible, aka the Kleene Star
          .*      0 or more of any character
      +         1 or more possible, aka the Kleene plus
          .+      1 or more of any character
      *?              
      -         Represents an inclusive range between characters, ex 2-4 or e-i
      {n}       exactly n repetitions, ex a{3} or .{3}
      {n,}      at least n repetitions, ex a{3,}
      {n,m}     inclusive n to m repeitions, ex {3,4}
      ^p        demands pattern begins at the start of the line
      [^p]      negates pattern
      p$        demands pattern end line
      \         Escape character
      \\        raw backslash
      []        encapsulates a pattern, any single character within the list
      ()        Captures (returns) the value inside the matched pattern, very powerful
                  Can nest further captures inside!
      (a|b)     Condiitonal OR matching the exact text, ex: (cats|dogs) matches the whole cats or dogs - can be used with explicit patterns
        
    Common Patterns
      [A-Z]     Capital letters
      [a-z]     Lowercase letters
      [0-9]     Digits
      [qwe]     A single-width character that can be q, w, or e
      [^qwe]    A single-width character that cannot be q, w, or e
   
    Back Referencing
      Effectively this uses your capture groups as "variables" 
      in dynamic or related regex systems, such as text editor search and replace.
      This is not standard in all regex, but useful to know nontheless.
      To backreference, one simply can refer to them by their capture group number order from left to right
      \0  typically refers to the original text
      \1  first capture group
      \2  second capture group, etc
    
    Common Match patterns
      Numbers with commas, decimals, and scientific notation
        ^-?\d+(,\d+)*(\.\d+(e\d+)?)?$
      Telephone numbers
        1?[\s-]?\(?(\d{3})\)?[\s-]?\d{3}[\s-]?\d{4}
        
      
      