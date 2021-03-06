## Changelog

Versioning complies with [semantic versioning (semver)](http://semver.org/).

<!-- NOTE: An entry template is automatically added each time `make version` is called. Fill in changes afterwards. -->

* **[v0.4.3](https://github.com/mklement0/typex/compare/v0.4.2...v0.4.3)** (2020-10-13):
  * [fix] npm v6.14.8 inexplicably complains about the "install" command in package.json (which simply printfs an informational message), so it is diabled for now.

* **[v0.4.2](https://github.com/mklement0/typex/compare/v0.4.1...v0.4.2)** (2020-10-13):
  * [fix] Syntax error fixed that was masked by an accidental non-breaking space Unicode char.

* **[v0.4.1](https://github.com/mklement0/typex/compare/v0.4.0...v0.4.1)** (2015-09-21):
  * [fix] `typex /` now works correctly.

* **[v0.4.0](https://github.com/mklement0/typex/compare/v0.3.3...v0.4.0)** (2015-09-21):
  * [potentially breaking change] `typex` now accepts options _after_ operands
      as well (except after `--`), and now also accepts long option names.
  * [doc] `typex` now has a man page (if manually installed, use `typex --man`);
      `typex -h` now just prints concise usage information.
  * [doc] Read-me improved.
  * [fix] Various fixes and stability improvements.
  * [dev] Installation of sourcing (with `-i`) no longer uses `ed` so as to
      work on a wider range of platforms, notably Fedora.
  * [dev] Tests improved, additional tests added.

* **[v0.3.3](https://github.com/mklement0/typex/compare/v0.3.2...v0.3.3)** (2015-09-15):
  * [dev] Makefile improvements; various other behind-the-scenes tweaks.

* **[v0.3.2](https://github.com/mklement0/typex/compare/v0.3.1...v0.3.2)** (2015-09-03):
  * [fix] Broken (dangling) symlinks are now properly detected and reported.

* **[v0.3.1](https://github.com/mklement0/typex/compare/v0.3.0...v0.3.1)** (2015-06-26):
  * [dev] Makefile updated; to-do file added; typo in source-code comment fixed.
  * [doc] Minor read-me revision.

* **[v0.3.0](https://github.com/mklement0/typex/compare/v0.2.1...v0.3.0)** (2015-06-10):
  * [behavior change, enhancement] When reporting on an alias, information about the underlying command is now output with indentation, so as to make it clear that the information is subordinate to the alias information.
  * [fix] Reporting on an alias' underlying command no longer causes additional command forms of the same name to be ignored.
  * [fix] Obtaining a file's last-modified timestamp no longer breaks with filenames with embedded spaces.
  * [doc] Read-me improvements; version badge switched to shields.io; license badge added.

* **v0.2.1** (2015-05-30):
  * [doc] [npm registry badge](https://badge.fury.io) added

* **v0.2.0** (2015-05-24):
  * [enhancement] Now by default prints information about the _current shell_ (if no names are given).
  * [enhancement] Specifying `.` now also prints the current directory's canonical path.
  * [enhancement] Given a filesystem path, now also displays its canonical path with all symlinks resolved, if different.
  * [enhancement] A warning is now issued if a bareword can't be found as a command, but a file or dir. of the same name exists in the current dir.
  * [enhancement] For aliases, their definitions are now printed recursively, if applicable, and, if the ultimate definition's first token is a command, its information is printed as well.
  * [fix] `typex perl` now correctly reports Perl's version.
  * [fix] Paths with embedded space are now handled correctly.

* **v0.1.7** (2015-03-04):
  * Fix: Variables `$u` and `$i` that happen to be defined in the current shell no longer interfere with the sourced function.

* **v0.1.6** (2015-02-11):
  * Temp. fix: `typex -i` now properly reports failure on platforms that don't have the actual `ed` line editor, such as Debian.

* **v0.1.5** (2015-02-11):
  * Fix: --version no longer mistakenly exits the current shell when typex is invoked as a sourced function.
  * Dev: bash-presence test improved.
  * Dev: Makefile improvements.

* **v0.1.4** (2015-02-11):
  * Fix: Filenames that start with '-' are now handled correctly.
  * Dev: bash-presence test added.
  * Dev: Makefile improvements.

* **v0.1.3** (2015-02-09):
  * Doc: read-me and package description improved.

* **v0.1.2** (2015-02-07):
  * Fix: sourcing no longer auto-installed/-removed on package installation - removed due to permission headaches; users must now run typex -i manually after installation.

* **v0.1.1** (2015-02-07):
  * Fix: --version reported incorrect version number.
  * Temp. fix: installation of sourcing with -i doesn't report error in case of failure so as not to prevent installation of the npm package altogether.

* **v0.1.0** (2015-02-07):
  * Initial release.
