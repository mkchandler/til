If you have to move a lot of files in Git at the same time, here is a helpful Bash script to do it:

```bash
for FILE in src/*.js; do git mv $FILE new-dir/; done
```

The first time I used this was when I needed to adjust the casing on file names while doing a JavaScript refactor. Since Windows is not case-sensitive, adjusting the file system did not affect Git.

Source: http://stackoverflow.com/a/2305537/54727
