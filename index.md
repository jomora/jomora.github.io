Hi there and welcome to my blog about computer science (CS).
From time to time, you will find new posts on a broad range of CS topics.

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
