On OSX, instead of using `sha1sum`, `sha256sum`, etc. like on Linux, you can use the `shasum` tool:

    shasum -c checksum-file

The default uses `SHA1`, but you can easily check against other algorithms using the `-a` option:

   shasum -a 256 -c checksum-file

