0.1.0.6
=======

- Use http2-client-0.5.0.0 or greater
- Detect http2 goaway frames and remove connections from the
  connection pool accordingly
- Detect connection errors when sending messages and remove
  connections from the pool when they happen
- Fix in the README: The parameter is not timeout, but
  parallelConnections

0.1.0.5
=======

- Bugfix: Close the cleanup thread when closing a session
- Check if the certificates and key exist early, when the session is created
- Catch IO errors and return a temporary failure instead
- Depend explicitly on http2-client-0.3.0.2 for now

0.1.0.4
=======

- Add an interactive/scriptable mode where messages are read from stdin
- Re-structure exports to improve readability of the documentation
- Close connections in addition to sending http2 gtfo when idle time exceeded (needs http2-client-0.3.0.2)
- Add a closeSession method
- Close sessions when they are garbage collected

0.1.0.3
=======

- Filter out invalid token characters when hex encoded tokens are supplied
- Clarify the documentation
- Close the flow control thread when closing connections

0.1.0.1
=======

- Initial release
