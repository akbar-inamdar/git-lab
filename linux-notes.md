# Linux Notes

## File system
- / is root; /home users; /etc config; /var/log logs; /tmp temp; /usr programs

## Commands
- pwd, ls -la, cd, cd .. (parent), cd ~ (home), cd - (previous)
- mkdir, touch, cat, cp, mv, rm (no recycle bin)
- > overwrites a file, >> appends
- man <command> shows the manual

## Permissions
- ls -l: type, owner, group, others (e.g. rw-r--r--)
- r=4, w=2, x=1 -> 644 = rw-r--r--, 755 = rwxr-xr-x
- chmod 644 file | chmod u+w file | chmod g-x file | chmod a+x file
- u=user, g=group, o=others, a=all; + add, - remove, = set

## Users and processes
- whoami, id, sudo (run as admin)
- sudo access on CentOS: usermod -aG wheel <user>
- ps aux | grep <name> (pipe | sends output to the next command)
- top shows live processes (q to quit)
