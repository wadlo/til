# Linux CLI Head

The `head` command allows you to just get the first N lines of something. For example you can grab the first 5 lines of a file with `head file.txt -n 1`

Its most useful feature though is that it can be piped into with other commands to grab just the first line that's returned. For example `grep 'hello world' file.txt | head -n 1`.