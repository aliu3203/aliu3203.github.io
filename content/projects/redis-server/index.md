---

title: Redis Server in Java
summary: A Redis-compatible server built from scratch to learn concurrency and how servers talk to clients
tech_stack:
 - Java
 - Maven
 - JUnit
status: 'WIP'

links:
  - type: github
    url: https://github.com/aliu3203/redis_server
    label: Code
---

A small project I started to learn concurrency and how servers actually talk to clients. It
speaks the Redis wire protocol, so you can point a normal `redis-cli` at it.

The parser reads off a byte buffer by hand rather than going through a library, since that was
the part I wanted to understand. Commands go through a dispatcher into a keyspace that is
split across striped locks, so two clients touching unrelated keys do not wait on each other.
Blocking commands like `BLPOP` park the client in a waiter queue instead of polling, which is
the piece I got wrong the most times before it worked.

There are tests on the parts that are easy to get subtly wrong: the parser, the locking, and
the blocking path.
