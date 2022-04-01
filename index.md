Hi there and welcome to my blog about computer science (CS).
From time to time, you will find new posts on a broad range of CS topics.

# 01.04.2021 TIL: How to install Haskell on a Mac (not a joke)

https://www.haskell.org/ghcup/

```sh
curl --proto '=https' --tlsv1.2 -sSf https://get-ghcup.haskell.org | sh
```

# 23.11.2021 TIL: How to swap stdin and stderr

```sh
<command> 3>&1 1>&2 2>&3
```
