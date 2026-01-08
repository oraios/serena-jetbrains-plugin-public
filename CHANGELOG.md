# 2023.2.6 (unreleased)

* Add type hierarchy retrieval
* Fix error message when symbol retrieval fails with non-unique symbol (report all symbol details)
* Fix free socket search on macOS and potentially other platforms (caused BindException; must use same listening address throughout)

# 2023.2.5 (2025-12-27)

* Fix symbol retrieval in GoLand

# 2023.2.4 (2025-12-25)

* Fix: Symbol rename operation could trigger a dialog in the presence
  of "dynamic references"; we prevent the dialog, renaming only 
  definite references
* Use listen address 127.0.0.1 for the service
* Fix use of deprecated/internal JetBrains APIs

# 2023.2.3 (2024-12-24)

* Improved symbols overview, adding depth parameter
* Reduce tasks running on the event dispatch thread (EDT) to a minimum
* Mark Rider IDE as unsupported

# 2023.2.2 (2025-12-19)

* Support IDE version 2025.3

# 2023.2.1 (2025-12-19)

* Initial release