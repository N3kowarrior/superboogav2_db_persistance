# superboogav2_db_persistence

`superboogav2_db_persistence` provides a patched version of `chromadb.py` (part of superboogav2) written to manage chromadb. This modified version introduces disk persistence for the database. The database files are stored in either of the following directories:

- `extensions/superboogav2/chromadb_persistent` (Linux)
- `extensions\superboogav2\chromadb_persistent` (Windows)

## Notes:

- Switching character is not properly implemented.
- Clear function does not delete the whole database but removes and recreates current collection.
- If issues persist, remove the path mentioned above.
