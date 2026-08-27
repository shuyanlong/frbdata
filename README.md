# Machine-Learning Clustering of Fast Radio Bursts

This repository contains the data and supplementary posterior results for the paper:

**Machine-Learning Clustering of Fast Radio Bursts: Implications for the Hubble Tension**

## Files

### `77frbdata_machine_learning_log_mst_pca_add_2feature.csv`

Processed data for the 77 localized FRBs used in the machine-learning and cosmological analyses.

The fiducial clustering uses six features:

- extragalactic dispersion measure, `DM_e`
- spectroscopic redshift, `zsp`
- spectral luminosity, `Lν`
- energy, `Energy`
- flux
- fluence

The luminosity and energy are calculated assuming a fiducial flat
\(\Lambda\)CDM cosmology with

\[
H_0=67.36~{\rm km\,s^{-1}\,Mpc^{-1}},\qquad
\Omega_m=0.3153,\qquad
\Omega_\Lambda=1-\Omega_m.
\]

The CSV also includes the PCA+K-means and MST cluster labels used in the paper.

As a control test, clustering is repeated using only flux and fluence,
excluding `DM_e`, `zsp`, `Lν`, and `Energy`. 

## Supplementary Posterior Contours

### `plot.pdf`

This file contains the full multidimensional posterior contours for the
FRB subsamples analyzed in the paper, including

\[
\theta,\quad F,\quad \mu,\quad \sigma_{\rm host},
\]

and the derived Hubble constant \(H_0\).

The PDF includes results for both the fiducial six-feature clustering and
the flux--fluence control analysis. These contours supplement the
marginalized \(H_0\) posteriors shown in the main manuscript and allow the
relations between \(H_0\) and the nuisance parameters to be inspected.

## Notes

The machine-learning clusters are not interpreted as established physical
FRB populations. The analysis is intended to test how possible FRB
substructure and sample composition affect the inferred Hubble constant.
