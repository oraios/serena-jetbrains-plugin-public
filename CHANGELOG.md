# 2023.2.11 (2026-03-03)

* Add configuration option "Open tool window at startup" (in IDE settings / Tools / Serena)

# 2023.2.10 (2026-02-18)

* File symbol overview can now retrieve quick info (signature information)
* Allow parallel requests
* Make requests appear in the IDE's status bar, allowing cancellation
* Extend range of compatible IDE versions to include 2026.1
* Fix: Change the file system refresh approach once again in order to avoid execution on the event dispatch thread (EDT).
  The earlier fix in 2023.2.8 was not effective in newer IDE versions. 
* Fix: Retrieval of DART symbols and references (particularly methods)
* Fix: Kotlin documentation/quick info retrieval (support target-based documentation API)

# 2023.2.9 (2026-01-22)

* Improve name path matching logic: At any level, require overload index to match
  only if it is specified in the matching expression

# 2023.2.8 (2026-01-19)

* Make the listen address configurable (in IDE settings / Tools / Serena)
* Make file system synchronisation before tool execution configurable (in IDE settings / Tools / Serena)
* Fix: Type hierarchy retrieval did not work for some languages, because
  the hierarchy type was not explicitly selected (e.g. Kotlin)
* Fix: Do not call file system refresh from the event dispatch thread (EDT).
  This could cause the IDE's UI to freeze temporarily.

# 2023.2.7 (2026-01-12)

* Fix: Name path computation & matching only considered overload indices at the leaf level
* Fix: Name resolution for Rust impl blocks (name path was null)

# 2023.2.6 (2026-01-11)

* New tool endpoints: type hierarchy retrieval (subtypes/supertypes) 
* Add further retrieval options for symbols (quick info/signature, documentation)
* Fix error message when symbol retrieval fails with non-unique symbol (report all symbol details)
* Fix free socket search on macOS and potentially other platforms (caused BindException; must use same listening address throughout)
* Differentiate between recoverable and non-recoverable exceptions, returning different status codes
* Fix log tab in Serena tool window being closeable

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