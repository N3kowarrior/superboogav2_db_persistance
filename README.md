superboogav2_db_persistence

superboogav2_db_persistence provides a patched version of chromadb.py (part of superboogav2) to manage chromadb with disk persistence. The database files are stored in the following directories:

    Linux: extensions/superboogav2/chromadb_persistent
    Windows: extensions\superboogav2\chromadb_persistent

About chat.py

chat.py is a native module from TGW (Text Generation Web UI) that I have hooked to retrieve the current name of the character. This extension will not be maintained indefinitely, as I may lose interest over time. Here is a quick guide on how to patch it for this extension:
Step 1: Add Custom Code

Add the following lines after the imports:

python

# Custom code
loaded_character_name = "name2"
def return_loaded_character_name():
    return loaded_character_name

This will ensure that the name of the character is retrieved and creates a variable for storing the character name.
Step 2: Modify the load_character Function

Locate the function called load_character, which might look like def load_character(character, name1, name2):. Then, add the following code at the first line of the function without removing any existing code:

python

# Custom code begins here
global loaded_character_name
loaded_character_name = character
# Custom code ends here!

Notes

    The clear function does not delete the entire database but removes and recreates the current collection.
    If issues persist, remove the path mentioned above.
