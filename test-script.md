---
title: "Test script"
author: "Favour Etinkumoh"
date: "2026-07-27"
output: 
  html_document: 
    keep_md: true
---


``` r
library(tidyverse)
```

```
## ── Attaching core tidyverse packages ──────────────────────── tidyverse 2.0.0 ──
## ✔ dplyr     1.2.1     ✔ readr     2.2.0
## ✔ forcats   1.0.1     ✔ stringr   1.6.0
## ✔ ggplot2   4.0.3     ✔ tibble    3.3.1
## ✔ lubridate 1.9.5     ✔ tidyr     1.3.2
## ✔ purrr     1.2.2     
## ── Conflicts ────────────────────────────────────────── tidyverse_conflicts() ──
## ✖ dplyr::filter() masks stats::filter()
## ✖ dplyr::lag()    masks stats::lag()
## ℹ Use the conflicted package (<http://conflicted.r-lib.org/>) to force all conflicts to become errors
```

``` r
dummy_data <- tibble(
  treatment = rep(c("Control", "Nephelinite", "Melilitolite"), each = 3),
  replicate = rep(1:3, times = 3),
  pH = c(
    4.7, 4.8, 4.9,
    5.3, 5.4, 5.5,
    6.0, 6.1, 6.2
  )
)

ggplot(dummy_data, aes(x = treatment, y = pH)) +
  geom_point(size = 3) +
  theme_classic()
```

![](test-script_files/figure-html/unnamed-chunk-1-1.png)<!-- -->

