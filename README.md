# node-red-contrib-fs-ops
A Node Red node for performing file system operations.

This node is a wrapper around many of the functions in Node's file system library, which in turn is a wrapper around the standard POSIX filesysem functions.

The nodes and functions provided are:

  * fs-ops-move - Move or rename files and directories
  * fs-ops-delete - Delete a file or directory
  * fs-ops-access - Test existence and accessibility of a file or directory
  * fs-ops-size - Get size of a file or directory in bytes
  * fs-ops-dir - Get array of file and directory names in a directory
  * fs-ops-mkdir - Make a new directory
  * fs-ops-mktmpdir - Make a new directory with a random unique name
  * fs-ops-file in - uncompress with zlib a file to a string

Parameters such as path and filename can be sourced from strings, or message, flow, or global property.  Likewise, results can be stored in a message, flow or global property.

The general design is that each node will pass the message if the action is successful, otherwise it will throw an exception and drop the message.
