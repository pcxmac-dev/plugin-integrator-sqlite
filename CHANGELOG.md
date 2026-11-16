# Changelog

## 0.1.0 (2026-11-16)

The first release: SQLite as a database plugin (plugin API 2.3, liminal-libs 1.61.0; the user, 2026-11-15: "for the
integrator i need plugins for each type of database and in each plugin can setup either new databases or connections
to existing databases using many different types of IP or IPC methods. each instance in the plugin has it's own
configuration how it's shared, ports, permissions etc").

- Its own instance `data`: the data folder's SQLite files, opened as the app opens them. With nothing set, nothing
  changes.
- New database (a file in `instances/` or at a whole path, in write-ahead logging, saying what it is) and Connect (a
  file that exists, kept only when it is a database).
- Two methods: `file`, and `helper` for a file on another system's drive, chosen by itself.
- Shares, kept to by the link's helper: a suite on another system reads, reads and writes, or does not attach.
- Its API card: SQLite through Python's sqlite3 module, every address one of sqlite.org's or python.org's own pages,
  read on 2026-11-16, with the three pages that say why a file is never opened across systems.
