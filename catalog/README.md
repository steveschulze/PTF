# Photometry and SED modelling catalogue

The file PTF_CCSN.fits has three layers/tables.

**1) General**

This table summarises the observed photometry in the AB system without any reddening correction. The table contains the following columns:

| Keyword           | Description                                                   |
| ----------------- | ------------------------------------------------------------- |
| OBJECT 		    | Object name                                                   |
| TYPE   		    | SN type                                                       |
| REDSHIFT   	    | Redshift                                                      |
| ZMETHOD   	    | How was the redshift measure? SDSS, NED, galaxy lines in the SN spectrum, SN template matching? |
| IAU_NAME 		    | IAU name                                                      |
| SN_RA_HMS		    | Right ascension of the SN in the HMS system                   |
| SN_DEC_DMS	    | Declination of the SN in the DMS system                       |
| HOST_RA_HMS	    | Right ascension of the host in the HMS system                 |
| HOST_DEC_DMS	    | Declination of the host in the DMS system                     |
| OFFSET	        | Projected distance between the SN and the host (unit: arcsec) |
| OFFSET_ERR	    | 1 sigma error                                                 |
| OFFSET_KPC	    | Projected distance between the SN and the host (unit: kpc)    |
| OFFSET_KPC_ERR	| 1 sigma error                                                 |

**2) Photometry**

This table summarises the observed photometry in the AB system without any reddeningcorrection. The table contains the following columns:

| Keyword               | Description                                            |
| --------------------- | ------------------------------------------------------ |
| OBJECT 	 			| Object name                                            |
| MAGOBS_{FILTER}		| Brightness in a given filter (if not available: -99 )  |
| MAGOBS_{FILTER}_ERR	| Photometric error (non-detections: -99)                |

Photometry is reported in the following bands (if data are available)

>GALEX_FUV, GALEX_NUV,
UVOT_UVW2, UVOT_UVM2, UVOT_UVW1, UVOT_U, UVOT_B, UVOT_V, 
SDSS_U, SDSS_G, SDSS_R, SDSS_I, SDSS_Z,
PANSTARRS_G, PANSTARRS_R, PANSTARRS_I, PANSTARRS_Z,PANSTARRS_Y,
JOHNSON_U, JOHNSON_B, BESSELL_V, COUSINS_R, BESSELL_I,
2MASS_J, 2MASS_H, 2MASS_KS,
F225W, F390W, F606W,
F105W, F110W, F125W, F140W, F160W,
IRAC_I1, IRAC_I2, IRAC_I3, IRAC_I4,
WISE_W1, WISE_W2


**3) SED_PROSPECTOR**

This table summarises the output from SED modelling with Prospector. The table contains thefollowing columns:
| Keyword       | Description                                            |
| ------------- | ------------------------------------------------------ |
| OBJECT 		| Object name                                            |
| REDSHIFT		| REDSHIFT                                               |
| CHI2_BEST		| chi^2 of the best fit                               |
| NOF_USED		| Numbers of filters used                                |
| MAGMOD_{FILTER}_INF/MED/SUP		| Model-predicted apparent magnitude (not corrected for host attenuration; INF, MED, SUP correspond to the 16, 50, 84%-iles)                |
| MAGABS_{FILTER}_INF/MED/SUP		| Absolute magnitude (not corrected for host attenuation; INF, MED, SUP correspond to the 16, 50, 84%-iles)                |
| MAGOBS_{FILTER}_INF/MED/SUP		| Observed magnitude (not corrected for host attenuation; contains an additional systematic error w.r.t. the magnitudes in "Photometry"; INF, MED, SUP correspond to the 16, 50, 84%-iles)                |
| EBVSTAR_INF/MED,SUP		| Stellar attentuation assuming the Calzetti model (unit: mag; INF, MED, SUP correspond to the 16, 50, 84%-iles)|
| TAGE_INF/MED,SUP		| Age of the light-weighted stellar population (unit: Gyr; INF, MED,SUP correspond to the 16, 50, 84%-iles)|
| TAU_INF/MED,SUP		| e-folding time scale of the lin-exp SFH (unit: Gyr; INF, MED, SUPcorrespond to the 16, 50, 84%-iles)|
| MASS_INF/MED,SUP		| Mass of the living stars (unit: solar masses; log units; INF, MED, SUPcorrespond to the 16, 50, 84%-iles)|
| SFR_INF/MED,SUP		| Recent star-formation rate (unit: solar masses/yr; log units; INF, MED,SUP correspond to the 16, 50, 84%-iles)|
| SSFR_INF/MED,SUP		| Specific SFR (unit: 1/yr; log units; INF, MED, SUP correspond to the 16, 50, 84%-iles)|

The model and absolute are reported only for filters where data were available and, in addition, in the FUV, B, V, R, g', r', K_s.