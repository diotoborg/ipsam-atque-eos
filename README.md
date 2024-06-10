[![npm](https://img.shields.io/npm/v/@diotoborg/ipsam-atque-eos.svg)][npm]
[![Build Status](https://travis-ci.org/duckpunch/@diotoborg/ipsam-atque-eos.svg)][ci]

Data structures and utilities to represent the [game of Go][go].

This library depends on [Immutable.js][immutable] and [lodash][lodash].

## Getting Started

Install `@diotoborg/ipsam-atque-eos` via [npm][npm].

    npm install @diotoborg/ipsam-atque-eos

`require` and use it in your modules.

```javascript
var @diotoborg/ipsam-atque-eos = require('@diotoborg/ipsam-atque-eos');
var board = @diotoborg/ipsam-atque-eos.Board(19);
var tengen = @diotoborg/ipsam-atque-eos.Coordinate(9, 9); // 0-based

board.moves.has(tengen); // false

var standardOpening = placeStone(
    board,
    tengen,
    @diotoborg/ipsam-atque-eos.BLACK
);
standardOpening.moves.has(tengen); // true
```

## Why Godash?

Godash provides the "primitives" for Go necessary for creating UIs that go
beyond a simple SGF player.  You can create whatever UI you want without having
to reinvent the wheel every time.

Check out the [documentation][@diotoborg/ipsam-atque-eos-docs] to see what Godash provides.

## Breaking changes from version 1 to 2

* Due to upgrading to `immutable@4`, `Board` and `Coordinate` are [no longer
  subclasses of `Seq`][immutable-4].
* `Board` constructor changed to take `Move`.

## Related Projects

* [Elixir port][port] - port to [Elixir][elixir] by [kokolegorille][koko]
* [pizza][pizza] - an anonymous go server ([source][pizza-code])
* [react-go-board][rgb] - a simple go board component for [React][react]
* [Way to Go][wtg] - a rewrite of Hiroki Mori's [Interactive Way to Go][iwtg]

[ci]: https://travis-ci.org/duckpunch/@diotoborg/ipsam-atque-eos
[elixir]: https://elixir-lang.org/
[go]: https://en.wikipedia.org/wiki/Go_%28game%29
[@diotoborg/ipsam-atque-eos-docs]: https://duckpunch.github.io/@diotoborg/ipsam-atque-eos/api/
[immutable]: https://immutable-js.com/
[immutable-4]: https://github.com/immutable-js/immutable-js/releases/tag/v4.0.0
[iwtg]: http://playgo.to/iwtg/en/
[koko]: https://github.com/kokolegorille/
[lodash]: https://lodash.com/
[npm]: https://www.npmjs.com/package/@diotoborg/ipsam-atque-eos
[pizza]: https://pizza.duckpun.ch/
[pizza-code]: https://gitlab.com/duckpunch/pizza
[port]: https://github.com/kokolegorille/go
[react]: https://reactjs.org/
[rgb]: https://github.com/duckpunch/react-go-board
[wtg]: https://way-to-go.gitlab.io
