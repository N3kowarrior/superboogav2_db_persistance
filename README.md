superboogav2_db_persistence

superboogav2_db_persistence provides a patched version of chromadb.py (part of superboogav2) to manage chromadb with disk persistence. The database files are stored in the following directories:

- `extensions/superboogav2/chromadb_persistent` (Linux)
- `extensions\superboogav2\chromadb_persistent` (Windows)

## About chat.py
"chat.py" is a native module from TGW (Text generation webui), which I've added hook to retrieve current name of character. This extension will go without maintanence, if or better when I loose interest.
So here a quick "guide" on how to patch it for this extension.:
Step 1:First add this on first free line after imports:
- #Custome code
- loaded_character_name = "name2"
- def return_loaded_character_name():
-    return loaded_character_name
This will ensure that name of character is retrieved and creates variable for storing the character name.
Step 2:
Locate function called "load_character" when it's defined, it might look like "def load_character(character, name1, name2):". Then paste this code at first line of the function. Do not remove any code just put it infront of that code.
-    #Custom code begins here
-    global loaded_character_name
-    loaded_character_name = character
-   #Custom code ends here!

## Notes:

- Clear function does not delete the whole database but removes and recreates current collection.
