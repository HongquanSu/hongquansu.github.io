---                                                                                                                                                                                                                                                             
layout: post
title: "Useful tools for Astronomy"
tagline: "python" "fits"
---

Read fits file using Python :
```
from astropy.io import fits
fits_file = fits.open(fits_in)
fits_head = fits_file[0].header
fits_data = fits_file[0].data
```
