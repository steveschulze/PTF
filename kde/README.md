# Probability distribution functions

We report the SEDs for redshifts, SN-host offsets (unit: kpc), observed $r'$ band magnitude, absolute $B$-band mag, galaxy mass, SFR, sSFR, age of the stellar population and the host attenuation. The file names have the following structure `kde_{SN_CLASS}_{PROPERTY}_v4.ascii`.

| SN_CLASS          | Additional notes                                               |
| ----------------- | ------------------------------------------------------------- |
| SLSN-I			|  |
| SNIc-BL			|  |
| SNIc				|  |
| SNIbc				| SNe which we couldn't decide between Ib and Ic |
| SNIb				|  |	
| SNIIb				|  |	
| SNII				|  |	
| SLSN-IIn			|  |
| SNIIn				|  |	
| SNIbn				|  |	


| PROPERTY          | Additional notes                                                    |
| ----------------- | ------------------------------------------------------------------- |
| redshift			| redshift                                                            |
| offset			| SN-host offset (unit: kpc)                                          |
| mr				| r-band magnitude; not corrected for host reddening                  |
| MB				| absolute magnitude in $B$-band; not corrected for host reddening    |
| mass				| mass of the living stars (unit: $M_\odot$; log system)              |	
| sfr				| current SFR (unit: $M_\odot$/yr; log system)                        | 
| ssfr			    | sSFR (unit: 1/yr; log system)                                       |
| tage			    | light-weighted age of the stellar-population (unit: yr; log system) |
| ebvstar			| host attenuation (unit: mag; Calzetti model)                        | 

Each file has four columns:

| Column          | Notes                                                    |
| --------------- | ---------------------------------------------------------|
| X               | x-value                                                  |
| KDE_INF         | 34% confidence interval                                  |
| KDE_MED         | 50% confidence interval (i.e. median)                    |
| KDE_SUP         | 84% confidence interval                                  |

Each probability distribution function is normalised to the maximum of `KDE_MED'.