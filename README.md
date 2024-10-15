ALGORITHM counter
VAR
  n : STRING;
  noc, now, nov : INTEGER;
  i : INTEGER;

BEGIN
  noc := 0;  
  now := 1;
  nov := 0;  
  i := 1;
  
  READ(n);
  
  FOR i FROM 1 TO LENGTH(n) DO
    noc := noc + 1;
    
    IF n[i] = " " or "."THEN
      now := now + 1;
    END_IF
    
    IF n[i] IN ("a", "e", "i", "o", "u", "A", "E", "I", "O", "U") THEN
      nov := nov + 1;
    END_IF
  END_FOR
  
  WRITE("Number of characters: ", noc);
  WRITE("Number of words: ", now);
  WRITE("Number of vowels: ", nov);
END
