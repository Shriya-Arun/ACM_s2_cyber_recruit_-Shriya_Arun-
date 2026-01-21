Challenge Description : Analyze the html file given and find the hidden flag. 

Analysis: Converted the text file to html and opened it in browser. Tried using assembleAndDecode(), built-in function but got no result. The concatenated string was not a valid base64. Decoded each of the base64 fragments individually for clues. Found a fragment which had to be decoded multiple times as it was a layered base64. The final decoded string was "TIM BERNERS-LEE". This was likely the flag because the challenge instruction had given a hint about html birth and Tim was the inventor of html. 
Command used to decode the fragments : echo "base64_fragment" | base64 -d 

Final flag: flag{TIM_BERNERS_LEE} 
