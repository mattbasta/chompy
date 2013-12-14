# Chompy

Chompy is a tool for testing code quality. Unlike code coverage, which only
guarantees that code is run, Chompy tests reverse code coverage, which
guarantees that code is run in a useful way.

This is accomplished by iterating over each node of a project's AST tree and
removing each it in turn. After a removal, the unit tests are run against the
updated code. If the unit tests don't fail, the AST node that was removed is
either non-functional or untested.

