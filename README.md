<!--

@license Apache-2.0

Copyright (c) 2018 The Stdlib Authors.

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

   http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.

-->


<details>
  <summary>
    About stdlib...
  </summary>
  <p>We believe in a future in which the web is a preferred environment for numerical computation. To help realize this future, we've built stdlib. stdlib is a standard library, with an emphasis on numerical and scientific computation, written in JavaScript (and C) for execution in browsers and in Node.js.</p>
  <p>The library is fully decomposable, being architected in such a way that you can swap out and mix and match APIs and functionality to cater to your exact preferences and use cases.</p>
  <p>When you use stdlib, you can be absolutely certain that you are using the most thorough, rigorous, well-written, studied, documented, tested, measured, and high-quality code out there.</p>
  <p>To join us in bringing numerical computing to the web, get started by checking us out on <a href="https://github.com/stdlib-js/stdlib">GitHub</a>, and please consider <a href="https://opencollective.com/stdlib">financially supporting stdlib</a>. We greatly appreciate your continued support!</p>
</details>

# Casting Modes

[![NPM version][npm-image]][npm-url] [![Build Status][test-image]][test-url] [![Coverage Status][coverage-image]][coverage-url] <!-- [![dependencies][dependencies-image]][dependencies-url] -->

> List of ndarray casting modes.

<!-- Section to include introductory text. Make sure to keep an empty line after the intro `section` element and another before the `/section` close. -->

<section class="intro">

</section>

<!-- /.intro -->

<!-- Package usage documentation. -->



<section class="usage">

## Usage

```javascript
import modes from 'https://cdn.jsdelivr.net/gh/stdlib-js/ndarray-casting-modes@esm/index.mjs';
```
The previous example will load the latest bundled code from the esm branch. Alternatively, you may load a specific version by loading the file from one of the [tagged bundles](https://github.com/stdlib-js/ndarray-casting-modes/tags). For example,

```javascript
import modes from 'https://cdn.jsdelivr.net/gh/stdlib-js/ndarray-casting-modes@v0.1.0-esm/index.mjs';
```

You can also import the following named exports from the package:

```javascript
import { enum } from 'https://cdn.jsdelivr.net/gh/stdlib-js/ndarray-casting-modes@esm/index.mjs';
```

#### modes()

Returns a list of ndarray casting modes.

```javascript
var out = modes();
// returns [ 'none', 'equiv', 'safe', 'same-kind', 'unsafe' ]
```

The output `array` contains the following modes:

-   `none`: only allow casting between identical types.
-   `equiv`: allow casting between identical and byte swapped types.
-   `safe`: only allow "safe" casts.
-   `same-kind`: allow "safe" casts and casts within the same kind (e.g., between signed integers or between floats).
-   `unsafe`: allow casting between all types (including between integers and floats).

</section>

<!-- /.usage -->

<!-- Package usage notes. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->

<section class="notes">

</section>

<!-- /.notes -->

<!-- Package usage examples. -->

<section class="examples">

## Examples

<!-- eslint no-undef: "error" -->

```html
<!DOCTYPE html>
<html lang="en">
<body>
<script type="module">

import indexOf from 'https://cdn.jsdelivr.net/gh/stdlib-js/utils-index-of@esm/index.mjs';
import modes from 'https://cdn.jsdelivr.net/gh/stdlib-js/ndarray-casting-modes@esm/index.mjs';

var MODES = modes();
var bool;

function isMode( str ) {
    if ( indexOf( MODES, str ) === -1 ) {
        return false;
    }
    return true;
}

bool = isMode( 'none' );
// returns true

bool = isMode( 'equiv' );
// returns true

bool = isMode( 'safe' );
// returns true

bool = isMode( 'same-kind' );
// returns true

bool = isMode( 'unsafe' );
// returns true

bool = isMode( 'beep' );
// returns false

</script>
</body>
</html>
```

</section>

<!-- /.examples -->

<!-- Section to include cited references. If references are included, add a horizontal rule *before* the section. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->

<section class="references">

</section>

<!-- /.references -->

<!-- Section for related `stdlib` packages. Do not manually edit this section, as it is automatically populated. -->

<section class="related">

* * *

## See Also

-   <span class="package-name">[`@stdlib/ndarray-array`][@stdlib/ndarray/array]</span><span class="delimiter">: </span><span class="description">multidimensional arrays.</span>
-   <span class="package-name">[`@stdlib/ndarray-ctor`][@stdlib/ndarray/ctor]</span><span class="delimiter">: </span><span class="description">multidimensional array constructor.</span>

</section>

<!-- /.related -->

<!-- Section for all links. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->


<section class="main-repo" >

* * *

## Notice

This package is part of [stdlib][stdlib], a standard library with an emphasis on numerical and scientific computing. The library provides a collection of robust, high performance libraries for mathematics, statistics, streams, utilities, and more.

For more information on the project, filing bug reports and feature requests, and guidance on how to develop [stdlib][stdlib], see the main project [repository][stdlib].

#### Community

[![Chat][chat-image]][chat-url]

---

## License

See [LICENSE][stdlib-license].


## Copyright

Copyright &copy; 2016-2023. The Stdlib [Authors][stdlib-authors].

</section>

<!-- /.stdlib -->

<!-- Section for all links. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->

<section class="links">

[npm-image]: http://img.shields.io/npm/v/@stdlib/ndarray-casting-modes.svg
[npm-url]: https://npmjs.org/package/@stdlib/ndarray-casting-modes

[test-image]: https://github.com/stdlib-js/ndarray-casting-modes/actions/workflows/test.yml/badge.svg?branch=v0.1.0
[test-url]: https://github.com/stdlib-js/ndarray-casting-modes/actions/workflows/test.yml?query=branch:v0.1.0

[coverage-image]: https://img.shields.io/codecov/c/github/stdlib-js/ndarray-casting-modes/main.svg
[coverage-url]: https://codecov.io/github/stdlib-js/ndarray-casting-modes?branch=main

<!--

[dependencies-image]: https://img.shields.io/david/stdlib-js/ndarray-casting-modes.svg
[dependencies-url]: https://david-dm.org/stdlib-js/ndarray-casting-modes/main

-->

[chat-image]: https://img.shields.io/gitter/room/stdlib-js/stdlib.svg
[chat-url]: https://app.gitter.im/#/room/#stdlib-js_stdlib:gitter.im

[stdlib]: https://github.com/stdlib-js/stdlib

[stdlib-authors]: https://github.com/stdlib-js/stdlib/graphs/contributors

[umd]: https://github.com/umdjs/umd
[es-module]: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Modules

[deno-url]: https://github.com/stdlib-js/ndarray-casting-modes/tree/deno
[umd-url]: https://github.com/stdlib-js/ndarray-casting-modes/tree/umd
[esm-url]: https://github.com/stdlib-js/ndarray-casting-modes/tree/esm
[branches-url]: https://github.com/stdlib-js/ndarray-casting-modes/blob/main/branches.md

[stdlib-license]: https://raw.githubusercontent.com/stdlib-js/ndarray-casting-modes/main/LICENSE

<!-- <related-links> -->

[@stdlib/ndarray/array]: https://github.com/stdlib-js/ndarray-array/tree/esm

[@stdlib/ndarray/ctor]: https://github.com/stdlib-js/ndarray-ctor/tree/esm

<!-- </related-links> -->

</section>

<!-- /.links -->
