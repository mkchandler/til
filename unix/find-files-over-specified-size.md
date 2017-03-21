While recently converting a 38,000+ file project over to Git, I realized that there were some very large database backups sprinkled throughout the directory structure. Since I did not want these committed to the Git repository, I needed an easy way to locate them.

I was able to find any files over 50 MB (which is when GitHub starts warning you about file size) by using the following command:

```bash
find . -size +50M -exec ls -lh {} \+
```

The `-size` argument allows various size increments, such as:

```
k   for Kilobytes (ex: +3000k)
M   for Megabytes (ex: +50M)
G   for Gigabytes (ex: +2G)
```

On a small side-note, there is a good explanation of why it uses `\+` instead of `\;` here: http://stackoverflow.com/a/6085237/54727