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



<section class="usage">

## Usage

```javascript
import ns from 'https://cdn.jsdelivr.net/gh/stdlib-js/stats-incr@deno/mod.js';
```

You can also import the following named exports from the package:

```javascript
import { incrapcorr, incrcount, incrcovariance, incrcovmat, incrcv, increwmean, increwstdev, increwvariance, incrgmean, incrgrubbs, incrhmean, incrkurtosis, incrmaape, incrmae, incrmapcorr, incrmape, incrmax, incrmaxabs, incrmcovariance, incrmcv, incrmda, incrme, incrmean, incrmeanabs, incrmeanabs2, incrmeanstdev, incrmeanvar, incrmgmean, incrmgrubbs, incrmhmean, incrmidrange, incrmin, incrminabs, incrminmax, incrminmaxabs, incrmmaape, incrmmae, incrmmape, incrmmax, incrmmaxabs, incrmmda, incrmme, incrmmean, incrmmeanabs, incrmmeanabs2, incrmmeanstdev, incrmmeanvar, incrmmidrange, incrmmin, incrmminabs, incrmminmax, incrmminmaxabs, incrmmpe, incrmmse, incrmpcorr, incrmpcorr2, incrmpcorrdist, incrmpe, incrmprod, incrmrange, incrmrmse, incrmrss, incrmse, incrmstdev, incrmsum, incrmsumabs, incrmsumabs2, incrmsummary, incrmsumprod, incrmvariance, incrmvmr, incrnancount, incrnansum, incrnansumabs, incrnansumabs2, incrpcorr, incrpcorr2, incrpcorrdist, incrpcorrdistmat, incrpcorrmat, incrprod, incrrange, incrrmse, incrrss, incrskewness, incrstdev, incrsum, incrsumabs, incrsumabs2, incrsummary, incrsumprod, incrvariance, incrvmr, incrwmean } from 'https://cdn.jsdelivr.net/gh/stdlib-js/stats-incr@deno/mod.js';
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
import getKeys from 'https://cdn.jsdelivr.net/gh/stdlib-js/utils-keys@deno/mod.js';
import ns from 'https://cdn.jsdelivr.net/gh/stdlib-js/stats-incr@deno/mod.js';

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

[npm-image]: http://img.shields.io/npm/v/@stdlib/stats-incr.svg
[npm-url]: https://npmjs.org/package/@stdlib/stats-incr

[test-image]: https://github.com/stdlib-js/stats-incr/actions/workflows/test.yml/badge.svg?branch=v0.1.0
[test-url]: https://github.com/stdlib-js/stats-incr/actions/workflows/test.yml?query=branch:v0.1.0

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
[umd-url]: https://github.com/stdlib-js/stats-incr/tree/umd
[esm-url]: https://github.com/stdlib-js/stats-incr/tree/esm
[branches-url]: https://github.com/stdlib-js/stats-incr/blob/main/branches.md

[stdlib-license]: https://raw.githubusercontent.com/stdlib-js/stats-incr/main/LICENSE

<!-- <toc-links> -->

[@stdlib/stats/incr/apcorr]: https://github.com/stdlib-js/stats-incr-apcorr/tree/deno

[@stdlib/stats/incr/count]: https://github.com/stdlib-js/stats-incr-count/tree/deno

[@stdlib/stats/incr/covariance]: https://github.com/stdlib-js/stats-incr-covariance/tree/deno

[@stdlib/stats/incr/covmat]: https://github.com/stdlib-js/stats-incr-covmat/tree/deno

[@stdlib/stats/incr/cv]: https://github.com/stdlib-js/stats-incr-cv/tree/deno

[@stdlib/stats/incr/ewmean]: https://github.com/stdlib-js/stats-incr-ewmean/tree/deno

[@stdlib/stats/incr/ewstdev]: https://github.com/stdlib-js/stats-incr-ewstdev/tree/deno

[@stdlib/stats/incr/ewvariance]: https://github.com/stdlib-js/stats-incr-ewvariance/tree/deno

[@stdlib/stats/incr/gmean]: https://github.com/stdlib-js/stats-incr-gmean/tree/deno

[@stdlib/stats/incr/grubbs]: https://github.com/stdlib-js/stats-incr-grubbs/tree/deno

[@stdlib/stats/incr/hmean]: https://github.com/stdlib-js/stats-incr-hmean/tree/deno

[@stdlib/stats/incr/kurtosis]: https://github.com/stdlib-js/stats-incr-kurtosis/tree/deno

[@stdlib/stats/incr/maape]: https://github.com/stdlib-js/stats-incr-maape/tree/deno

[@stdlib/stats/incr/mae]: https://github.com/stdlib-js/stats-incr-mae/tree/deno

[@stdlib/stats/incr/mapcorr]: https://github.com/stdlib-js/stats-incr-mapcorr/tree/deno

[@stdlib/stats/incr/mape]: https://github.com/stdlib-js/stats-incr-mape/tree/deno

[@stdlib/stats/incr/max]: https://github.com/stdlib-js/stats-incr-max/tree/deno

[@stdlib/stats/incr/maxabs]: https://github.com/stdlib-js/stats-incr-maxabs/tree/deno

[@stdlib/stats/incr/mcovariance]: https://github.com/stdlib-js/stats-incr-mcovariance/tree/deno

[@stdlib/stats/incr/mcv]: https://github.com/stdlib-js/stats-incr-mcv/tree/deno

[@stdlib/stats/incr/mda]: https://github.com/stdlib-js/stats-incr-mda/tree/deno

[@stdlib/stats/incr/me]: https://github.com/stdlib-js/stats-incr-me/tree/deno

[@stdlib/stats/incr/mean]: https://github.com/stdlib-js/stats-incr-mean/tree/deno

[@stdlib/stats/incr/meanabs]: https://github.com/stdlib-js/stats-incr-meanabs/tree/deno

[@stdlib/stats/incr/meanabs2]: https://github.com/stdlib-js/stats-incr-meanabs2/tree/deno

[@stdlib/stats/incr/meanstdev]: https://github.com/stdlib-js/stats-incr-meanstdev/tree/deno

[@stdlib/stats/incr/meanvar]: https://github.com/stdlib-js/stats-incr-meanvar/tree/deno

[@stdlib/stats/incr/mgmean]: https://github.com/stdlib-js/stats-incr-mgmean/tree/deno

[@stdlib/stats/incr/mgrubbs]: https://github.com/stdlib-js/stats-incr-mgrubbs/tree/deno

[@stdlib/stats/incr/mhmean]: https://github.com/stdlib-js/stats-incr-mhmean/tree/deno

[@stdlib/stats/incr/midrange]: https://github.com/stdlib-js/stats-incr-midrange/tree/deno

[@stdlib/stats/incr/min]: https://github.com/stdlib-js/stats-incr-min/tree/deno

[@stdlib/stats/incr/minabs]: https://github.com/stdlib-js/stats-incr-minabs/tree/deno

[@stdlib/stats/incr/minmax]: https://github.com/stdlib-js/stats-incr-minmax/tree/deno

[@stdlib/stats/incr/minmaxabs]: https://github.com/stdlib-js/stats-incr-minmaxabs/tree/deno

[@stdlib/stats/incr/mmaape]: https://github.com/stdlib-js/stats-incr-mmaape/tree/deno

[@stdlib/stats/incr/mmae]: https://github.com/stdlib-js/stats-incr-mmae/tree/deno

[@stdlib/stats/incr/mmape]: https://github.com/stdlib-js/stats-incr-mmape/tree/deno

[@stdlib/stats/incr/mmax]: https://github.com/stdlib-js/stats-incr-mmax/tree/deno

[@stdlib/stats/incr/mmaxabs]: https://github.com/stdlib-js/stats-incr-mmaxabs/tree/deno

[@stdlib/stats/incr/mmda]: https://github.com/stdlib-js/stats-incr-mmda/tree/deno

[@stdlib/stats/incr/mme]: https://github.com/stdlib-js/stats-incr-mme/tree/deno

[@stdlib/stats/incr/mmean]: https://github.com/stdlib-js/stats-incr-mmean/tree/deno

[@stdlib/stats/incr/mmeanabs]: https://github.com/stdlib-js/stats-incr-mmeanabs/tree/deno

[@stdlib/stats/incr/mmeanabs2]: https://github.com/stdlib-js/stats-incr-mmeanabs2/tree/deno

[@stdlib/stats/incr/mmeanstdev]: https://github.com/stdlib-js/stats-incr-mmeanstdev/tree/deno

[@stdlib/stats/incr/mmeanvar]: https://github.com/stdlib-js/stats-incr-mmeanvar/tree/deno

[@stdlib/stats/incr/mmidrange]: https://github.com/stdlib-js/stats-incr-mmidrange/tree/deno

[@stdlib/stats/incr/mmin]: https://github.com/stdlib-js/stats-incr-mmin/tree/deno

[@stdlib/stats/incr/mminabs]: https://github.com/stdlib-js/stats-incr-mminabs/tree/deno

[@stdlib/stats/incr/mminmax]: https://github.com/stdlib-js/stats-incr-mminmax/tree/deno

[@stdlib/stats/incr/mminmaxabs]: https://github.com/stdlib-js/stats-incr-mminmaxabs/tree/deno

[@stdlib/stats/incr/mmpe]: https://github.com/stdlib-js/stats-incr-mmpe/tree/deno

[@stdlib/stats/incr/mmse]: https://github.com/stdlib-js/stats-incr-mmse/tree/deno

[@stdlib/stats/incr/mpcorr]: https://github.com/stdlib-js/stats-incr-mpcorr/tree/deno

[@stdlib/stats/incr/mpcorr2]: https://github.com/stdlib-js/stats-incr-mpcorr2/tree/deno

[@stdlib/stats/incr/mpcorrdist]: https://github.com/stdlib-js/stats-incr-mpcorrdist/tree/deno

[@stdlib/stats/incr/mpe]: https://github.com/stdlib-js/stats-incr-mpe/tree/deno

[@stdlib/stats/incr/mprod]: https://github.com/stdlib-js/stats-incr-mprod/tree/deno

[@stdlib/stats/incr/mrange]: https://github.com/stdlib-js/stats-incr-mrange/tree/deno

[@stdlib/stats/incr/mrmse]: https://github.com/stdlib-js/stats-incr-mrmse/tree/deno

[@stdlib/stats/incr/mrss]: https://github.com/stdlib-js/stats-incr-mrss/tree/deno

[@stdlib/stats/incr/mse]: https://github.com/stdlib-js/stats-incr-mse/tree/deno

[@stdlib/stats/incr/mstdev]: https://github.com/stdlib-js/stats-incr-mstdev/tree/deno

[@stdlib/stats/incr/msum]: https://github.com/stdlib-js/stats-incr-msum/tree/deno

[@stdlib/stats/incr/msumabs]: https://github.com/stdlib-js/stats-incr-msumabs/tree/deno

[@stdlib/stats/incr/msumabs2]: https://github.com/stdlib-js/stats-incr-msumabs2/tree/deno

[@stdlib/stats/incr/msummary]: https://github.com/stdlib-js/stats-incr-msummary/tree/deno

[@stdlib/stats/incr/msumprod]: https://github.com/stdlib-js/stats-incr-msumprod/tree/deno

[@stdlib/stats/incr/mvariance]: https://github.com/stdlib-js/stats-incr-mvariance/tree/deno

[@stdlib/stats/incr/mvmr]: https://github.com/stdlib-js/stats-incr-mvmr/tree/deno

[@stdlib/stats/incr/nancount]: https://github.com/stdlib-js/stats-incr-nancount/tree/deno

[@stdlib/stats/incr/nansum]: https://github.com/stdlib-js/stats-incr-nansum/tree/deno

[@stdlib/stats/incr/nansumabs]: https://github.com/stdlib-js/stats-incr-nansumabs/tree/deno

[@stdlib/stats/incr/nansumabs2]: https://github.com/stdlib-js/stats-incr-nansumabs2/tree/deno

[@stdlib/stats/incr/pcorr]: https://github.com/stdlib-js/stats-incr-pcorr/tree/deno

[@stdlib/stats/incr/pcorr2]: https://github.com/stdlib-js/stats-incr-pcorr2/tree/deno

[@stdlib/stats/incr/pcorrdist]: https://github.com/stdlib-js/stats-incr-pcorrdist/tree/deno

[@stdlib/stats/incr/pcorrdistmat]: https://github.com/stdlib-js/stats-incr-pcorrdistmat/tree/deno

[@stdlib/stats/incr/pcorrmat]: https://github.com/stdlib-js/stats-incr-pcorrmat/tree/deno

[@stdlib/stats/incr/prod]: https://github.com/stdlib-js/stats-incr-prod/tree/deno

[@stdlib/stats/incr/range]: https://github.com/stdlib-js/stats-incr-range/tree/deno

[@stdlib/stats/incr/rmse]: https://github.com/stdlib-js/stats-incr-rmse/tree/deno

[@stdlib/stats/incr/rss]: https://github.com/stdlib-js/stats-incr-rss/tree/deno

[@stdlib/stats/incr/skewness]: https://github.com/stdlib-js/stats-incr-skewness/tree/deno

[@stdlib/stats/incr/stdev]: https://github.com/stdlib-js/stats-incr-stdev/tree/deno

[@stdlib/stats/incr/sum]: https://github.com/stdlib-js/stats-incr-sum/tree/deno

[@stdlib/stats/incr/sumabs]: https://github.com/stdlib-js/stats-incr-sumabs/tree/deno

[@stdlib/stats/incr/sumabs2]: https://github.com/stdlib-js/stats-incr-sumabs2/tree/deno

[@stdlib/stats/incr/summary]: https://github.com/stdlib-js/stats-incr-summary/tree/deno

[@stdlib/stats/incr/sumprod]: https://github.com/stdlib-js/stats-incr-sumprod/tree/deno

[@stdlib/stats/incr/variance]: https://github.com/stdlib-js/stats-incr-variance/tree/deno

[@stdlib/stats/incr/vmr]: https://github.com/stdlib-js/stats-incr-vmr/tree/deno

[@stdlib/stats/incr/wmean]: https://github.com/stdlib-js/stats-incr-wmean/tree/deno

<!-- </toc-links> -->

</section>

<!-- /.links -->
