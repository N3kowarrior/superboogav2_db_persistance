superboogav2_db_persistence

superboogav2_db_persistence is a patched version of chromadb.py designed to manage chromadb. This modified version introduces disk persistence for the database. The database files are stored in either of the following directories:

    extensions/superboogav2/chromadb_persistent
    extensions\superboogav2\chromadb_persistent

Additional parameters required for the database operation are saved in chroma_data.json, located in:

    extensions/superboogav2/chroma_data.json
    extensions\superboogav2\chroma_data.json

Notes:

    If the clear function fails, deleting both the file and the folder will initiate the creation of a new database.
