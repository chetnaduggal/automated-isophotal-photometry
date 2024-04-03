# Aperture photometry for HST, PanSTARRS and WISE imaging 

An extensively used method of measuring photometry for extended sources like galaxies in the literature is isophotal analysis, i.e., fitting elliptical isophotes to derive radial profiles.  Here this is done with the [ellipse](http://stsdas.stsci.edu/documents/SUG/UG_33.html) routine in [Python-based IRAF](https://iraf-community.github.io/pyraf.html).

Unrelated neighboring galaxies and stars are masked out prior to the fitting. The isophotal profiles (surface brightness, ellipticity, position angle vs. radial distance) are extracted from the images in the form of an ASCII table. Photometry is derived based on the 1σ isophote - the isophote with intensity 1 standard deviation above the mean of the sky background - which is selected as the outermost isophote and used as the integration aperture. Systematic uncertainty in the computed magnitudes is derived by adding the Poisson noise in source flux and RMS error from the sky background, in quadrature.

The photometric measurements were corrected for Galactic extinction using the scaling relation by Cardelli et al. (1989) and the E(B−V) color excess sourced from the [NASA/IPAC]( https://irsa.ipac.caltech.edu/applications/DUST/) archive. 

----------------------------
### Data 

The code and results in this repository were part of the analysis done for a newly published study in ApJ, [Duggal et al. 2024](https://iopscience.iop.org/article/10.3847/1538-4357/ad2513). The imaging observations used here are publicly available in [Hubble](https://mast.stsci.edu/portal/Mashup/Clients/Mast/Portal.html), [PanSTARRS](http://ps1images.stsci.edu/cgi-bin/ps1cutouts) and [WISE](https://irsa.ipac.caltech.edu/Missions/wise.html) data archives. 
