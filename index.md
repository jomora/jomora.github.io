Hi there and welcome to my blog about computer science (CS).
From time to time, you will find new posts on a broad range of CS topics.

# 23.11.2021 TIL: How to swap stdin and stderr

```sh
<command> 3>&1 1>&2 2>&3
```
