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
```

## File transfer

```bash
scp -r user@your.server.example.com:/path/to/foo /home/user/Desktop/
scp user@your.server.example.com:/path/to/foo/file /home/user/Desktop/file
```
