Hi there and welcome to my blog about computer science (CS).
From time to time, you will find new posts on a broad range of CS topics.

# 01.06.2023 How to test that a HTTP server is available on a specific port?

Recently, I faced the issue that a I used a minimal Ubuntu VM on Azure to test that a web server is reachable.
Unfortunately, neither netcat nor telnet, wget or curl were installed - the only tools where I knew at that time to test the connectivity to a HTTP server.
This was unfortunate especially because I was in a debugging session with colleague from another department and even `apt` did somehow not work.

Later, I remembered that you can create a TCP connection via the file system. A here's the solution:

```sh
# Create a file descriptor in the running terminal that can both read from and write to the file located at 
exec 3<>/dev/tcp/<hostname>/80
# Send the HTTP message to the file descriptor
printf "GET / HTTP/1.1\n\n" >&3
# Read the response from the file descriptor
cat <&3
```

Copied and adapted from here:
https://bash-prompt.net/guides/bash-sockets/

# 02.12.2022 A process won't help your dysfunctional team

"So don't deceive yourself into thinking that a process will just solve a dysfunctional team's problems" - Billy Hollis

https://youtu.be/cADdwFk2-7U?t=3109

# 22.11.2022 Why I'm eager to be able to know the intricacies of the tools I use

In the following video Jack Rusher talks about historical issues that influence how we build our software.

https://youtu.be/8Ab3ArE8W3s?t=1012

I think he's right in his critique.
However, since these old-fashioned tools like (pseudo) ttys are still around, we should know them by heart until better options emerge.


# 01.04.2021 TIL: How to install Haskell on a Mac (not a joke)

https://www.haskell.org/ghcup/

```sh
curl --proto '=https' --tlsv1.2 -sSf https://get-ghcup.haskell.org | sh
```

# 23.11.2021 TIL: How to swap stdin and stderr

```sh
<command> 3>&1 1>&2 2>&3
```
