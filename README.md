superboogav2_db_persistence

superboogav2_db_persistence provides patched version of chromadb.py (part of superboogav2 written to manage chromadb). This modified version introduces disk persistence for the database. The database files are stored in either of the following directories:

    extensions/superboogav2/chromadb_persistent    (linux)
    extensions\superboogav2\chromadb_persistent    (Windows)

Additional parameters required for the database operation are saved in chroma_data.json, located in:

    extensions/superboogav2/chroma_data.json    (linux)
    extensions\superboogav2\chroma_data.json    (Windows)

Notes:

    If the clear function fails, deleting both the file and the folder will initiate the creation of a new database. Also this patch was tested under linux.
↓(This) ↓
![obrazek](https://github.com/N3kowarriorCZenchilada/superboogav2_db_persistance/assets/118403968/ec0c5a73-2e72-4d6b-bd6b-70c1fc6a2da8)
