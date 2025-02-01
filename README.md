# Node.js Server Unresponsiveness

This repository demonstrates a common Node.js issue: server unresponsiveness caused by a long-running synchronous operation within the request handler.  The `server.js` file contains the buggy code.  The `serverSolution.js` file provides a solution using asynchronous operations and promises.

**Problem:**  Synchronous operations block the Node.js event loop.  This prevents the server from handling other requests while the long operation is in progress, resulting in unresponsiveness and potentially dropped connections.

**Solution:** Use asynchronous operations (e.g., timers, promises, async/await) to prevent blocking the event loop.  This allows the server to remain responsive while handling long-running tasks.