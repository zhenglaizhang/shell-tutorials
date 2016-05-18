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


Don't use cat as some are mentioned here. cat is a program while echo and printf are bash (shell) builtins. Launching a program or an other script (also mentioned above) means create an new process with all it's costs. Using builtins, writing functions are quite cheap, because there is no need to create (execute) a process (-environment).

The opner asks "is there any standard tool to output (pipe) to stderr", the schort answer is : NO ... why? ... rediredcting pipes is an elemantary concept in systems like unix (Linux...) and bash (sh) builds up on these concepts.

I agree with the opener that redirecting with notations like this: &2>1 is not very pleasant for modern programmers, but that's bash. Bash was not intended to write huge and robust programs, it is intended to help the admins to get there work with less keypresses ;-)

And at least, you can place the redirection anywhere in the line:

    $ echo This message >&2 goes to stderr 
This message goes to stderr
