# Aperture photometry for HST, PanSTARRS and WISE imaging 

AN extensively used method of measuring photometry for extended sources like galaxies in the literature is isophotal analysis, i.e., fitting elliptical isophotes to derive radial profiles.  Here this is done with the [ellipse](http://stsdas.stsci.edu/documents/SUG/UG_33.html) routine in [Python-based IRAF](https://iraf-community.github.io/pyraf.html).
Unrelated neighboring galaxies and stars were masked out prior to the fitting. The isophotal profiles (surface brightness, ellipticity, and position angle (PA) versus radial distance) extracted from the images. Photometry was derived based on the 1σ isophote - the isophote with intensity 1 standard deviation above the mean of the sky background - which is selected as the outermost isophote and used as the integration aperture. Systematic uncertainty in the computed magnitudes was derived by adding the Poisson noise in source flux and rms error from the sky background, in quadrature.

The photometric measurements were corrected for Galactic extinction using the scaling relation by Cardelli et al. (1989) and the E(B−V) color excess sourced from the NASA/IPAC archive. 

----------------------------
Data 

Hubble , PanSTARRS, WISE observation archives
