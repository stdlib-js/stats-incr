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

# Incremental Statistics

[![NPM version][npm-image]][npm-url] [![Build Status][test-image]][test-url] [![Coverage Status][coverage-image]][coverage-url] <!-- [![dependencies][dependencies-image]][dependencies-url] -->

> Incremental statistics.

<section class="installation">

## Installation

```bash
npm install @stdlib/stats-incr
```

Alternatively,

-   To load the package in a website via a `script` tag without installation and bundlers, use the [ES Module][es-module] available on the [`esm`][esm-url] branch (see [README][esm-readme]).
-   If you are using Deno, visit the [`deno`][deno-url] branch (see [README][deno-readme] for usage intructions).
-   For use in Observable, or in browser/node environments, use the [Universal Module Definition (UMD)][umd] build available on the [`umd`][umd-url] branch (see [README][umd-readme]).

The [branches.md][branches-url] file summarizes the available branches and displays a diagram illustrating their relationships.

To view installation and usage instructions specific to each branch build, be sure to explicitly navigate to the respective README files on each branch, as linked to above.

</section>

<section class="usage">

## Usage

```javascript
var ns = require( '@stdlib/stats-incr' );
```

#### ns

Namespace containing functions for computing statistics incrementally.

```javascript
var incr = ns;
// returns {...}
```

<!-- <toc pattern="*"> -->

<div class="namespace-toc">

-   <span class="signature">[`incrapcorr( [mx, my] )`][@stdlib/stats/incr/apcorr]</span><span class="delimiter">: </span><span class="description">compute a sample absolute Pearson product-moment correlation coefficient incrementally.</span>
-   <span class="signature">[`incrcount()`][@stdlib/stats/incr/count]</span><span class="delimiter">: </span><span class="description">compute a count incrementally.</span>
-   <span class="signature">[`incrcovariance( [mx, my] )`][@stdlib/stats/incr/covariance]</span><span class="delimiter">: </span><span class="description">compute an unbiased sample covariance incrementally.</span>
-   <span class="signature">[`incrcovmat( out[, means] )`][@stdlib/stats/incr/covmat]</span><span class="delimiter">: </span><span class="description">compute an unbiased sample covariance matrix incrementally.</span>
-   <span class="signature">[`incrcv( [mean] )`][@stdlib/stats/incr/cv]</span><span class="delimiter">: </span><span class="description">compute the coefficient of variation (CV) incrementally.</span>
-   <span class="signature">[`increwmean( alpha )`][@stdlib/stats/incr/ewmean]</span><span class="delimiter">: </span><span class="description">compute an exponentially weighted mean incrementally.</span>
-   <span class="signature">[`increwstdev( alpha )`][@stdlib/stats/incr/ewstdev]</span><span class="delimiter">: </span><span class="description">compute an exponentially weighted standard deviation incrementally.</span>
-   <span class="signature">[`increwvariance( alpha )`][@stdlib/stats/incr/ewvariance]</span><span class="delimiter">: </span><span class="description">compute an exponentially weighted variance incrementally.</span>
-   <span class="signature">[`incrgmean()`][@stdlib/stats/incr/gmean]</span><span class="delimiter">: </span><span class="description">compute a geometric mean incrementally.</span>
-   <span class="signature">[`incrgrubbs( [options] )`][@stdlib/stats/incr/grubbs]</span><span class="delimiter">: </span><span class="description">grubbs' test for outliers.</span>
-   <span class="signature">[`incrhmean()`][@stdlib/stats/incr/hmean]</span><span class="delimiter">: </span><span class="description">compute a harmonic mean incrementally.</span>
-   <span class="signature">[`incrkurtosis()`][@stdlib/stats/incr/kurtosis]</span><span class="delimiter">: </span><span class="description">compute a corrected sample excess kurtosis incrementally.</span>
-   <span class="signature">[`incrmaape()`][@stdlib/stats/incr/maape]</span><span class="delimiter">: </span><span class="description">compute the mean arctangent absolute percentage error (MAAPE) incrementally.</span>
-   <span class="signature">[`incrmae()`][@stdlib/stats/incr/mae]</span><span class="delimiter">: </span><span class="description">compute the mean absolute error (MAE) incrementally.</span>
-   <span class="signature">[`incrmapcorr( window[, mx, my] )`][@stdlib/stats/incr/mapcorr]</span><span class="delimiter">: </span><span class="description">compute a moving sample absolute Pearson product-moment correlation coefficient incrementally.</span>
-   <span class="signature">[`incrmape()`][@stdlib/stats/incr/mape]</span><span class="delimiter">: </span><span class="description">compute the mean absolute percentage error (MAPE) incrementally.</span>
-   <span class="signature">[`incrmax()`][@stdlib/stats/incr/max]</span><span class="delimiter">: </span><span class="description">compute a maximum value incrementally.</span>
-   <span class="signature">[`incrmaxabs()`][@stdlib/stats/incr/maxabs]</span><span class="delimiter">: </span><span class="description">compute a maximum absolute value incrementally.</span>
-   <span class="signature">[`incrmcovariance( window[, mx, my] )`][@stdlib/stats/incr/mcovariance]</span><span class="delimiter">: </span><span class="description">compute a moving unbiased sample covariance incrementally.</span>
-   <span class="signature">[`incrmcv( window[, mean] )`][@stdlib/stats/incr/mcv]</span><span class="delimiter">: </span><span class="description">compute a moving coefficient of variation (CV) incrementally.</span>
-   <span class="signature">[`incrmda()`][@stdlib/stats/incr/mda]</span><span class="delimiter">: </span><span class="description">compute the mean directional accuracy (MDA) incrementally.</span>
-   <span class="signature">[`incrme()`][@stdlib/stats/incr/me]</span><span class="delimiter">: </span><span class="description">compute the mean error (ME) incrementally.</span>
-   <span class="signature">[`incrmean()`][@stdlib/stats/incr/mean]</span><span class="delimiter">: </span><span class="description">compute an arithmetic mean incrementally.</span>
-   <span class="signature">[`incrmeanabs()`][@stdlib/stats/incr/meanabs]</span><span class="delimiter">: </span><span class="description">compute an arithmetic mean of absolute values incrementally.</span>
-   <span class="signature">[`incrmeanabs2()`][@stdlib/stats/incr/meanabs2]</span><span class="delimiter">: </span><span class="description">compute an arithmetic mean of squared absolute values incrementally.</span>
-   <span class="signature">[`incrmeanstdev( [out] )`][@stdlib/stats/incr/meanstdev]</span><span class="delimiter">: </span><span class="description">compute an arithmetic mean and a corrected sample standard deviation incrementally.</span>
-   <span class="signature">[`incrmeanvar( [out] )`][@stdlib/stats/incr/meanvar]</span><span class="delimiter">: </span><span class="description">compute an arithmetic mean and an unbiased sample variance incrementally.</span>
-   <span class="signature">[`incrmgmean( window )`][@stdlib/stats/incr/mgmean]</span><span class="delimiter">: </span><span class="description">compute a moving geometric mean incrementally.</span>
-   <span class="signature">[`incrmgrubbs( window[, options] )`][@stdlib/stats/incr/mgrubbs]</span><span class="delimiter">: </span><span class="description">moving Grubbs' test for outliers.</span>
-   <span class="signature">[`incrmhmean( window )`][@stdlib/stats/incr/mhmean]</span><span class="delimiter">: </span><span class="description">compute a moving harmonic mean incrementally.</span>
-   <span class="signature">[`incrmidrange()`][@stdlib/stats/incr/midrange]</span><span class="delimiter">: </span><span class="description">compute a mid-range incrementally.</span>
-   <span class="signature">[`incrmin()`][@stdlib/stats/incr/min]</span><span class="delimiter">: </span><span class="description">compute a minimum value incrementally.</span>
-   <span class="signature">[`incrminabs()`][@stdlib/stats/incr/minabs]</span><span class="delimiter">: </span><span class="description">compute a minimum absolute value incrementally.</span>
-   <span class="signature">[`incrminmax( [out] )`][@stdlib/stats/incr/minmax]</span><span class="delimiter">: </span><span class="description">compute a minimum and maximum incrementally.</span>
-   <span class="signature">[`incrminmaxabs( [out] )`][@stdlib/stats/incr/minmaxabs]</span><span class="delimiter">: </span><span class="description">compute minimum and maximum absolute values incrementally.</span>
-   <span class="signature">[`incrmmaape( window )`][@stdlib/stats/incr/mmaape]</span><span class="delimiter">: </span><span class="description">compute a moving mean arctangent absolute percentage error (MAAPE) incrementally.</span>
-   <span class="signature">[`incrmmae( window )`][@stdlib/stats/incr/mmae]</span><span class="delimiter">: </span><span class="description">compute a moving mean absolute error (MAE) incrementally.</span>
-   <span class="signature">[`incrmmape( window )`][@stdlib/stats/incr/mmape]</span><span class="delimiter">: </span><span class="description">compute a moving mean absolute percentage error incrementally.</span>
-   <span class="signature">[`incrmmax( window )`][@stdlib/stats/incr/mmax]</span><span class="delimiter">: </span><span class="description">compute a moving maximum value incrementally.</span>
-   <span class="signature">[`incrmmaxabs( window )`][@stdlib/stats/incr/mmaxabs]</span><span class="delimiter">: </span><span class="description">compute a moving maximum absolute value incrementally.</span>
-   <span class="signature">[`incrmmda( window )`][@stdlib/stats/incr/mmda]</span><span class="delimiter">: </span><span class="description">compute a moving mean directional accuracy (MDA) incrementally.</span>
-   <span class="signature">[`incrmme( window )`][@stdlib/stats/incr/mme]</span><span class="delimiter">: </span><span class="description">compute a moving mean error (ME) incrementally.</span>
-   <span class="signature">[`incrmmean( window )`][@stdlib/stats/incr/mmean]</span><span class="delimiter">: </span><span class="description">compute a moving arithmetic mean incrementally.</span>
-   <span class="signature">[`incrmmeanabs( window )`][@stdlib/stats/incr/mmeanabs]</span><span class="delimiter">: </span><span class="description">compute a moving arithmetic mean of absolute values incrementally.</span>
-   <span class="signature">[`incrmmeanabs2( window )`][@stdlib/stats/incr/mmeanabs2]</span><span class="delimiter">: </span><span class="description">compute a moving arithmetic mean of squared absolute values incrementally.</span>
-   <span class="signature">[`incrmmeanstdev( [out,] window )`][@stdlib/stats/incr/mmeanstdev]</span><span class="delimiter">: </span><span class="description">compute a moving arithmetic mean and corrected sample standard deviation incrementally.</span>
-   <span class="signature">[`incrmmeanvar( [out,] window )`][@stdlib/stats/incr/mmeanvar]</span><span class="delimiter">: </span><span class="description">compute a moving arithmetic mean and unbiased sample variance incrementally.</span>
-   <span class="signature">[`incrmmidrange( window )`][@stdlib/stats/incr/mmidrange]</span><span class="delimiter">: </span><span class="description">compute a moving mid-range incrementally.</span>
-   <span class="signature">[`incrmmin( window )`][@stdlib/stats/incr/mmin]</span><span class="delimiter">: </span><span class="description">compute a moving minimum value incrementally.</span>
-   <span class="signature">[`incrmminabs( window )`][@stdlib/stats/incr/mminabs]</span><span class="delimiter">: </span><span class="description">compute a moving minimum absolute value incrementally.</span>
-   <span class="signature">[`incrmminmax( [out,] window )`][@stdlib/stats/incr/mminmax]</span><span class="delimiter">: </span><span class="description">compute a moving minimum and maximum incrementally.</span>
-   <span class="signature">[`incrmminmaxabs( [out,] window )`][@stdlib/stats/incr/mminmaxabs]</span><span class="delimiter">: </span><span class="description">compute moving minimum and maximum absolute values incrementally.</span>
-   <span class="signature">[`incrmmpe( window )`][@stdlib/stats/incr/mmpe]</span><span class="delimiter">: </span><span class="description">compute a moving mean percentage error (MPE) incrementally.</span>
-   <span class="signature">[`incrmmse( window )`][@stdlib/stats/incr/mmse]</span><span class="delimiter">: </span><span class="description">compute a moving mean squared error (MSE) incrementally.</span>
-   <span class="signature">[`incrmpcorr( window[, mx, my] )`][@stdlib/stats/incr/mpcorr]</span><span class="delimiter">: </span><span class="description">compute a moving sample Pearson product-moment correlation coefficient incrementally.</span>
-   <span class="signature">[`incrmpcorr2( window[, mx, my] )`][@stdlib/stats/incr/mpcorr2]</span><span class="delimiter">: </span><span class="description">compute a moving squared sample Pearson product-moment correlation coefficient incrementally.</span>
-   <span class="signature">[`incrmpcorrdist( window[, mx, my] )`][@stdlib/stats/incr/mpcorrdist]</span><span class="delimiter">: </span><span class="description">compute a moving sample Pearson product-moment correlation distance incrementally.</span>
-   <span class="signature">[`incrmpe()`][@stdlib/stats/incr/mpe]</span><span class="delimiter">: </span><span class="description">compute the mean percentage error (MPE) incrementally.</span>
-   <span class="signature">[`incrmprod( window )`][@stdlib/stats/incr/mprod]</span><span class="delimiter">: </span><span class="description">compute a moving product incrementally.</span>
-   <span class="signature">[`incrmrange( window )`][@stdlib/stats/incr/mrange]</span><span class="delimiter">: </span><span class="description">compute a moving range incrementally.</span>
-   <span class="signature">[`incrmrmse( window )`][@stdlib/stats/incr/mrmse]</span><span class="delimiter">: </span><span class="description">compute a moving root mean squared error (RMSE) incrementally.</span>
-   <span class="signature">[`incrmrss( window )`][@stdlib/stats/incr/mrss]</span><span class="delimiter">: </span><span class="description">compute a moving residual sum of squares (RSS) incrementally.</span>
-   <span class="signature">[`incrmse()`][@stdlib/stats/incr/mse]</span><span class="delimiter">: </span><span class="description">compute the mean squared error (MSE) incrementally.</span>
-   <span class="signature">[`incrmstdev( window[, mean] )`][@stdlib/stats/incr/mstdev]</span><span class="delimiter">: </span><span class="description">compute a moving corrected sample standard deviation incrementally.</span>
-   <span class="signature">[`incrmsum( window )`][@stdlib/stats/incr/msum]</span><span class="delimiter">: </span><span class="description">compute a moving sum incrementally.</span>
-   <span class="signature">[`incrmsumabs( window )`][@stdlib/stats/incr/msumabs]</span><span class="delimiter">: </span><span class="description">compute a moving sum of absolute values incrementally.</span>
-   <span class="signature">[`incrmsumabs2( window )`][@stdlib/stats/incr/msumabs2]</span><span class="delimiter">: </span><span class="description">compute a moving sum of squared absolute values incrementally.</span>
-   <span class="signature">[`incrmsummary( window )`][@stdlib/stats/incr/msummary]</span><span class="delimiter">: </span><span class="description">compute a moving statistical summary incrementally.</span>
-   <span class="signature">[`incrmsumprod( window )`][@stdlib/stats/incr/msumprod]</span><span class="delimiter">: </span><span class="description">compute a moving sum of products incrementally.</span>
-   <span class="signature">[`incrmvariance( window[, mean] )`][@stdlib/stats/incr/mvariance]</span><span class="delimiter">: </span><span class="description">compute a moving unbiased sample variance incrementally.</span>
-   <span class="signature">[`incrmvmr( window[, mean] )`][@stdlib/stats/incr/mvmr]</span><span class="delimiter">: </span><span class="description">compute a moving variance-to-mean ratio (VMR) incrementally.</span>
-   <span class="signature">[`incrnancount()`][@stdlib/stats/incr/nancount]</span><span class="delimiter">: </span><span class="description">compute a count incrementally, ignoring `NaN` values.</span>
-   <span class="signature">[`incrnansum()`][@stdlib/stats/incr/nansum]</span><span class="delimiter">: </span><span class="description">compute a sum incrementally, ignoring `NaN` values.</span>
-   <span class="signature">[`incrnansumabs()`][@stdlib/stats/incr/nansumabs]</span><span class="delimiter">: </span><span class="description">compute a sum of absolute values incrementally, ignoring `NaN` values.</span>
-   <span class="signature">[`incrnansumabs2()`][@stdlib/stats/incr/nansumabs2]</span><span class="delimiter">: </span><span class="description">compute a sum of squared absolute values incrementally, ignoring `NaN` values.</span>
-   <span class="signature">[`incrpcorr( [mx, my] )`][@stdlib/stats/incr/pcorr]</span><span class="delimiter">: </span><span class="description">compute a sample Pearson product-moment correlation coefficient incrementally.</span>
-   <span class="signature">[`incrpcorr2( [mx, my] )`][@stdlib/stats/incr/pcorr2]</span><span class="delimiter">: </span><span class="description">compute a squared sample Pearson product-moment correlation coefficient incrementally.</span>
-   <span class="signature">[`incrpcorrdist( [mx, my] )`][@stdlib/stats/incr/pcorrdist]</span><span class="delimiter">: </span><span class="description">compute a sample Pearson product-moment correlation distance incrementally.</span>
-   <span class="signature">[`incrpcorrdistmat( out[, means] )`][@stdlib/stats/incr/pcorrdistmat]</span><span class="delimiter">: </span><span class="description">compute a sample Pearson product-moment correlation distance matrix incrementally.</span>
-   <span class="signature">[`incrpcorrmat( out[, means] )`][@stdlib/stats/incr/pcorrmat]</span><span class="delimiter">: </span><span class="description">compute a sample Pearson product-moment correlation matrix incrementally.</span>
-   <span class="signature">[`incrprod()`][@stdlib/stats/incr/prod]</span><span class="delimiter">: </span><span class="description">compute a product incrementally.</span>
-   <span class="signature">[`incrrange()`][@stdlib/stats/incr/range]</span><span class="delimiter">: </span><span class="description">compute a range incrementally.</span>
-   <span class="signature">[`incrrmse()`][@stdlib/stats/incr/rmse]</span><span class="delimiter">: </span><span class="description">compute the root mean squared error (RMSE) incrementally.</span>
-   <span class="signature">[`incrrss()`][@stdlib/stats/incr/rss]</span><span class="delimiter">: </span><span class="description">compute the residual sum of squares (RSS) incrementally.</span>
-   <span class="signature">[`incrskewness()`][@stdlib/stats/incr/skewness]</span><span class="delimiter">: </span><span class="description">compute a corrected sample skewness incrementally.</span>
-   <span class="signature">[`incrstdev( [mean] )`][@stdlib/stats/incr/stdev]</span><span class="delimiter">: </span><span class="description">compute a corrected sample standard deviation incrementally.</span>
-   <span class="signature">[`incrsum()`][@stdlib/stats/incr/sum]</span><span class="delimiter">: </span><span class="description">compute a sum incrementally.</span>
-   <span class="signature">[`incrsumabs()`][@stdlib/stats/incr/sumabs]</span><span class="delimiter">: </span><span class="description">compute a sum of absolute values incrementally.</span>
-   <span class="signature">[`incrsumabs2()`][@stdlib/stats/incr/sumabs2]</span><span class="delimiter">: </span><span class="description">compute a sum of squared absolute values incrementally.</span>
-   <span class="signature">[`incrsummary()`][@stdlib/stats/incr/summary]</span><span class="delimiter">: </span><span class="description">compute a statistical summary incrementally.</span>
-   <span class="signature">[`incrsumprod()`][@stdlib/stats/incr/sumprod]</span><span class="delimiter">: </span><span class="description">compute a sum of products incrementally.</span>
-   <span class="signature">[`incrvariance( [mean] )`][@stdlib/stats/incr/variance]</span><span class="delimiter">: </span><span class="description">compute an unbiased sample variance incrementally.</span>
-   <span class="signature">[`incrvmr( [mean] )`][@stdlib/stats/incr/vmr]</span><span class="delimiter">: </span><span class="description">compute a variance-to-mean ratio (VMR) incrementally.</span>
-   <span class="signature">[`incrwmean()`][@stdlib/stats/incr/wmean]</span><span class="delimiter">: </span><span class="description">compute a weighted arithmetic mean incrementally.</span>

</div>

<!-- </toc> -->

</section>

<!-- /.usage -->

<section class="examples">

## Examples

<!-- TODO: better examples -->

<!-- eslint no-undef: "error" -->

```javascript
var getKeys = require( '@stdlib/utils-keys' );
var ns = require( '@stdlib/stats-incr' );

console.log( getKeys( ns ) );
```

</section>

<!-- /.examples -->

<!-- Section for related `stdlib` packages. Do not manually edit this section, as it is automatically populated. -->

<section class="related">

</section>

<!-- /.related -->

<!-- Section for all links. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->


<section class="main-repo" >

* * *

## Notice

This package is part of [stdlib][stdlib], a standard library for JavaScript and Node.js, with an emphasis on numerical and scientific computing. The library provides a collection of robust, high performance libraries for mathematics, statistics, streams, utilities, and more.

For more information on the project, filing bug reports and feature requests, and guidance on how to develop [stdlib][stdlib], see the main project [repository][stdlib].

#### Community

[![Chat][chat-image]][chat-url]

---

## License

See [LICENSE][stdlib-license].


## Copyright

Copyright &copy; 2016-2025. The Stdlib [Authors][stdlib-authors].

</section>

<!-- /.stdlib -->

<!-- Section for all links. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->

<section class="links">

[npm-image]: http://img.shields.io/npm/v/@stdlib/stats-incr.svg
[npm-url]: https://npmjs.org/package/@stdlib/stats-incr

[test-image]: https://github.com/stdlib-js/stats-incr/actions/workflows/test.yml/badge.svg?branch=main
[test-url]: https://github.com/stdlib-js/stats-incr/actions/workflows/test.yml?query=branch:main

[coverage-image]: https://img.shields.io/codecov/c/github/stdlib-js/stats-incr/main.svg
[coverage-url]: https://codecov.io/github/stdlib-js/stats-incr?branch=main

<!--

[dependencies-image]: https://img.shields.io/david/stdlib-js/stats-incr.svg
[dependencies-url]: https://david-dm.org/stdlib-js/stats-incr/main

-->

[chat-image]: https://img.shields.io/gitter/room/stdlib-js/stdlib.svg
[chat-url]: https://app.gitter.im/#/room/#stdlib-js_stdlib:gitter.im

[stdlib]: https://github.com/stdlib-js/stdlib

[stdlib-authors]: https://github.com/stdlib-js/stdlib/graphs/contributors

[umd]: https://github.com/umdjs/umd
[es-module]: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Modules

[deno-url]: https://github.com/stdlib-js/stats-incr/tree/deno
[deno-readme]: https://github.com/stdlib-js/stats-incr/blob/deno/README.md
[umd-url]: https://github.com/stdlib-js/stats-incr/tree/umd
[umd-readme]: https://github.com/stdlib-js/stats-incr/blob/umd/README.md
[esm-url]: https://github.com/stdlib-js/stats-incr/tree/esm
[esm-readme]: https://github.com/stdlib-js/stats-incr/blob/esm/README.md
[branches-url]: https://github.com/stdlib-js/stats-incr/blob/main/branches.md

[stdlib-license]: https://raw.githubusercontent.com/stdlib-js/stats-incr/main/LICENSE

<!-- <toc-links> -->

[@stdlib/stats/incr/apcorr]: https://github.com/stdlib-js/stats-incr-apcorr

[@stdlib/stats/incr/count]: https://github.com/stdlib-js/stats-incr-count

[@stdlib/stats/incr/covariance]: https://github.com/stdlib-js/stats-incr-covariance

[@stdlib/stats/incr/covmat]: https://github.com/stdlib-js/stats-incr-covmat

[@stdlib/stats/incr/cv]: https://github.com/stdlib-js/stats-incr-cv

[@stdlib/stats/incr/ewmean]: https://github.com/stdlib-js/stats-incr-ewmean

[@stdlib/stats/incr/ewstdev]: https://github.com/stdlib-js/stats-incr-ewstdev

[@stdlib/stats/incr/ewvariance]: https://github.com/stdlib-js/stats-incr-ewvariance

[@stdlib/stats/incr/gmean]: https://github.com/stdlib-js/stats-incr-gmean

[@stdlib/stats/incr/grubbs]: https://github.com/stdlib-js/stats-incr-grubbs

[@stdlib/stats/incr/hmean]: https://github.com/stdlib-js/stats-incr-hmean

[@stdlib/stats/incr/kurtosis]: https://github.com/stdlib-js/stats-incr-kurtosis

[@stdlib/stats/incr/maape]: https://github.com/stdlib-js/stats-incr-maape

[@stdlib/stats/incr/mae]: https://github.com/stdlib-js/stats-incr-mae

[@stdlib/stats/incr/mapcorr]: https://github.com/stdlib-js/stats-incr-mapcorr

[@stdlib/stats/incr/mape]: https://github.com/stdlib-js/stats-incr-mape

[@stdlib/stats/incr/max]: https://github.com/stdlib-js/stats-incr-max

[@stdlib/stats/incr/maxabs]: https://github.com/stdlib-js/stats-incr-maxabs

[@stdlib/stats/incr/mcovariance]: https://github.com/stdlib-js/stats-incr-mcovariance

[@stdlib/stats/incr/mcv]: https://github.com/stdlib-js/stats-incr-mcv

[@stdlib/stats/incr/mda]: https://github.com/stdlib-js/stats-incr-mda

[@stdlib/stats/incr/me]: https://github.com/stdlib-js/stats-incr-me

[@stdlib/stats/incr/mean]: https://github.com/stdlib-js/stats-incr-mean

[@stdlib/stats/incr/meanabs]: https://github.com/stdlib-js/stats-incr-meanabs

[@stdlib/stats/incr/meanabs2]: https://github.com/stdlib-js/stats-incr-meanabs2

[@stdlib/stats/incr/meanstdev]: https://github.com/stdlib-js/stats-incr-meanstdev

[@stdlib/stats/incr/meanvar]: https://github.com/stdlib-js/stats-incr-meanvar

[@stdlib/stats/incr/mgmean]: https://github.com/stdlib-js/stats-incr-mgmean

[@stdlib/stats/incr/mgrubbs]: https://github.com/stdlib-js/stats-incr-mgrubbs

[@stdlib/stats/incr/mhmean]: https://github.com/stdlib-js/stats-incr-mhmean

[@stdlib/stats/incr/midrange]: https://github.com/stdlib-js/stats-incr-midrange

[@stdlib/stats/incr/min]: https://github.com/stdlib-js/stats-incr-min

[@stdlib/stats/incr/minabs]: https://github.com/stdlib-js/stats-incr-minabs

[@stdlib/stats/incr/minmax]: https://github.com/stdlib-js/stats-incr-minmax

[@stdlib/stats/incr/minmaxabs]: https://github.com/stdlib-js/stats-incr-minmaxabs

[@stdlib/stats/incr/mmaape]: https://github.com/stdlib-js/stats-incr-mmaape

[@stdlib/stats/incr/mmae]: https://github.com/stdlib-js/stats-incr-mmae

[@stdlib/stats/incr/mmape]: https://github.com/stdlib-js/stats-incr-mmape

[@stdlib/stats/incr/mmax]: https://github.com/stdlib-js/stats-incr-mmax

[@stdlib/stats/incr/mmaxabs]: https://github.com/stdlib-js/stats-incr-mmaxabs

[@stdlib/stats/incr/mmda]: https://github.com/stdlib-js/stats-incr-mmda

[@stdlib/stats/incr/mme]: https://github.com/stdlib-js/stats-incr-mme

[@stdlib/stats/incr/mmean]: https://github.com/stdlib-js/stats-incr-mmean

[@stdlib/stats/incr/mmeanabs]: https://github.com/stdlib-js/stats-incr-mmeanabs

[@stdlib/stats/incr/mmeanabs2]: https://github.com/stdlib-js/stats-incr-mmeanabs2

[@stdlib/stats/incr/mmeanstdev]: https://github.com/stdlib-js/stats-incr-mmeanstdev

[@stdlib/stats/incr/mmeanvar]: https://github.com/stdlib-js/stats-incr-mmeanvar

[@stdlib/stats/incr/mmidrange]: https://github.com/stdlib-js/stats-incr-mmidrange

[@stdlib/stats/incr/mmin]: https://github.com/stdlib-js/stats-incr-mmin

[@stdlib/stats/incr/mminabs]: https://github.com/stdlib-js/stats-incr-mminabs

[@stdlib/stats/incr/mminmax]: https://github.com/stdlib-js/stats-incr-mminmax

[@stdlib/stats/incr/mminmaxabs]: https://github.com/stdlib-js/stats-incr-mminmaxabs

[@stdlib/stats/incr/mmpe]: https://github.com/stdlib-js/stats-incr-mmpe

[@stdlib/stats/incr/mmse]: https://github.com/stdlib-js/stats-incr-mmse

[@stdlib/stats/incr/mpcorr]: https://github.com/stdlib-js/stats-incr-mpcorr

[@stdlib/stats/incr/mpcorr2]: https://github.com/stdlib-js/stats-incr-mpcorr2

[@stdlib/stats/incr/mpcorrdist]: https://github.com/stdlib-js/stats-incr-mpcorrdist

[@stdlib/stats/incr/mpe]: https://github.com/stdlib-js/stats-incr-mpe

[@stdlib/stats/incr/mprod]: https://github.com/stdlib-js/stats-incr-mprod

[@stdlib/stats/incr/mrange]: https://github.com/stdlib-js/stats-incr-mrange

[@stdlib/stats/incr/mrmse]: https://github.com/stdlib-js/stats-incr-mrmse

[@stdlib/stats/incr/mrss]: https://github.com/stdlib-js/stats-incr-mrss

[@stdlib/stats/incr/mse]: https://github.com/stdlib-js/stats-incr-mse

[@stdlib/stats/incr/mstdev]: https://github.com/stdlib-js/stats-incr-mstdev

[@stdlib/stats/incr/msum]: https://github.com/stdlib-js/stats-incr-msum

[@stdlib/stats/incr/msumabs]: https://github.com/stdlib-js/stats-incr-msumabs

[@stdlib/stats/incr/msumabs2]: https://github.com/stdlib-js/stats-incr-msumabs2

[@stdlib/stats/incr/msummary]: https://github.com/stdlib-js/stats-incr-msummary

[@stdlib/stats/incr/msumprod]: https://github.com/stdlib-js/stats-incr-msumprod

[@stdlib/stats/incr/mvariance]: https://github.com/stdlib-js/stats-incr-mvariance

[@stdlib/stats/incr/mvmr]: https://github.com/stdlib-js/stats-incr-mvmr

[@stdlib/stats/incr/nancount]: https://github.com/stdlib-js/stats-incr-nancount

[@stdlib/stats/incr/nansum]: https://github.com/stdlib-js/stats-incr-nansum

[@stdlib/stats/incr/nansumabs]: https://github.com/stdlib-js/stats-incr-nansumabs

[@stdlib/stats/incr/nansumabs2]: https://github.com/stdlib-js/stats-incr-nansumabs2

[@stdlib/stats/incr/pcorr]: https://github.com/stdlib-js/stats-incr-pcorr

[@stdlib/stats/incr/pcorr2]: https://github.com/stdlib-js/stats-incr-pcorr2

[@stdlib/stats/incr/pcorrdist]: https://github.com/stdlib-js/stats-incr-pcorrdist

[@stdlib/stats/incr/pcorrdistmat]: https://github.com/stdlib-js/stats-incr-pcorrdistmat

[@stdlib/stats/incr/pcorrmat]: https://github.com/stdlib-js/stats-incr-pcorrmat

[@stdlib/stats/incr/prod]: https://github.com/stdlib-js/stats-incr-prod

[@stdlib/stats/incr/range]: https://github.com/stdlib-js/stats-incr-range

[@stdlib/stats/incr/rmse]: https://github.com/stdlib-js/stats-incr-rmse

[@stdlib/stats/incr/rss]: https://github.com/stdlib-js/stats-incr-rss

[@stdlib/stats/incr/skewness]: https://github.com/stdlib-js/stats-incr-skewness

[@stdlib/stats/incr/stdev]: https://github.com/stdlib-js/stats-incr-stdev

[@stdlib/stats/incr/sum]: https://github.com/stdlib-js/stats-incr-sum

[@stdlib/stats/incr/sumabs]: https://github.com/stdlib-js/stats-incr-sumabs

[@stdlib/stats/incr/sumabs2]: https://github.com/stdlib-js/stats-incr-sumabs2

[@stdlib/stats/incr/summary]: https://github.com/stdlib-js/stats-incr-summary

[@stdlib/stats/incr/sumprod]: https://github.com/stdlib-js/stats-incr-sumprod

[@stdlib/stats/incr/variance]: https://github.com/stdlib-js/stats-incr-variance

[@stdlib/stats/incr/vmr]: https://github.com/stdlib-js/stats-incr-vmr

[@stdlib/stats/incr/wmean]: https://github.com/stdlib-js/stats-incr-wmean

<!-- </toc-links> -->

</section>

<!-- /.links -->
