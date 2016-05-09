# event-driven architecture

We use Amazon's Simple Queue Service and Simple Notifications Service to create
event messaging systems for our event-driven applications.  See details [here](https://github.com/emmadev/architecture/blob/master/docs/eda-on-aws.md).

[eda-core](https://github.com/emmadev/eda-core) is Emma's own opinionated library with concrete and abstract implementations of tools needed to build an event-driven service.

[eda-boilerplate](https://github.com/emmadev/eda-boilerplate) is a ready-to-go repository which implements a barebones event-driven service built on top of `eda-core`.

To get familiar with `eda-boilerplate`, try working through this [quick start
tutorial](https://github.com/emmadev/architecture/blob/master/docs/a-game-of-pong.md).
