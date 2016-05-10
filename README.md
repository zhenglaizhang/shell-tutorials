# shell-tutorials
Shell tutorials and common snippets

## Common commands

```bash
cd ~ && rm -rf dir1 dir2
chmod -R 755 ~/the-dir
chomd -R group:user ~/the-dir
```
### Usage

```bash
# view tcp/udp port usage
sudo lsof -iTCP -sTCP:LISTEN -n -P

# view c file numbers
find . -name "*\.[hc]" -print | wc –l
# view file content numbers
find . -name "*\.[hc]" -print | xargs wc -l | tail -n1
```

## File transfer

```bash
scp -r user@your.server.example.com:/path/to/foo /home/user/Desktop/
scp user@your.server.example.com:/path/to/foo/file /home/user/Desktop/file
```

## Network commands

```bash
route get localhost
route -v get localhost


traceroute www.baidu.com
```


## Data Analysis

```bash
cat file | uniq -c | sort -nr | head -5
du -chs

```

## Tips

    mkdir -p dir
    cd $_


    killall -KILL php-fpm
