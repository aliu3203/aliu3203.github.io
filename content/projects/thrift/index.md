---

title: Thrift
summary: A social app for thrift and vintage stores. Post a fit, tag where each piece came from
tech_stack:
 - TypeScript
 - React Native
 - Supabase
 - PostgreSQL
status: 'WIP'

links:
  - type: github
    url: https://github.com/daniu98/thrift
    label: Code
---

Built with [daniu98](https://github.com/daniu98). The idea came out of a gap we kept running
into: Google Maps knows a thrift store exists, but nothing tells you what is actually on the
racks right now, so the app has to generate that data itself.

You post an outfit and tag each piece with the store you found it at. Your friends see the
fit, and over time the stores build up a record of what people have actually been finding
there. It is a React Native app on a Supabase and Postgres backend, and we split the work by
feature rather than by frontend and backend.

Nothing has shipped yet. We are still building toward a version worth putting in front of
people.
