# RSG Mass-Loss Implementation (Vink & Sabhahit 2023)

MESA Inlist and run_star_extras file to reproduce the results from [Vink & Sabhahit (2023)](https://ui.adsabs.harvard.edu/abs/2023A%26A...678L...3V/abstract) - New mass-loss rates for red supergiants and other cool massive stars

**Links:**
- https://www.aanda.org/articles/aa/pdf/2023/10/aa47801-23.pdf
- https://ui.adsabs.harvard.edu/abs/2023A%26A...678L...3V/abstract

# Overview

Mass loss for red supergiants (RSGs) oft use empirical prescriptions like de Jager et al. (1988) with mass-loss scaling with luminosity. However, Yang et al. 2023 showcase an empirical mass-loss kink with the mass loss scaling steeply above log(L/L☉) of 4.5. We formulate a mass loss scaling with the luminosity to current mass ratio based on these empirical rates transitioning from a shallow to steep scaling. The paper is available at <a href="https://ui.adsabs.harvard.edu/abs/2023A%26A...678L...3V/abstract" target="_blank">Vink & Sabhahit (2023)</a> - Exploring the Red Supergiant wind kink. A Universal mass-loss concept for massive stars.


### Summary of Mass Loss Used

1. **O stars:** Vink et al. (2000, 2001)
2. **VMS:** Scaling from [Vink et al. (2011)](https://ui.adsabs.harvard.edu/abs/2011A%26A...531A.132V/abstract) and absolute rate fixed by the concept of transition mass loss point from [Vink & Gräfener (2012)](https://ui.adsabs.harvard.edu/abs/2012ApJ...751L..34V/abstract) calibrated to Arches cluster in the Galaxy and 30 Dor in the LMC
3. **WR stars:** Sander & Vink (2020)
4. **Red supergiants:** [Vink & Sabhahit (2023)](https://ui.adsabs.harvard.edu/abs/2023A%26A...678L...3V/abstract) - new mass-loss prescription with mass loss scaling switch from shallow to steep following Yang et al. 2023


## Relevant Files and What They Do

**MESA version:** r12115 (or specify your version)

1. **`inlist_project`**: MESA inlist file
2. **`/src/run_star_extras.f`**: run_stars file with the Vink & Sabhahit (2023) RSG mass loss implementation

## Usage

Compile the provided `run_star_extras.f` file. Modify `inlist_project` to set the initial mass. 

**Grid parameter range:**
- **Mass range:** 10-40 M☉ 
- **Evolutionary phases:** Red supergiant phase evolution
  
## Citation

If you use this mass loss implementation in your research, please cite:
```bibtex
@ARTICLE{2023A&A...678L...3V,
       author = {{Vink}, Jorick S. and {Sabhahit}, Gautham N.},
        title = "{Exploring the Red Supergiant wind kink. A Universal mass-loss concept for massive stars}",
      journal = {\aap},
     keywords = {stars: mass-loss, stars: massive, supergiants, stars: evolution, Astrophysics - Solar and Stellar Astrophysics, Astrophysics - Astrophysics of Galaxies, Astrophysics - High Energy Astrophysical Phenomena},
         year = 2023,
        month = oct,
       volume = {678},
          eid = {L3},
        pages = {L3},
          doi = {10.1051/0004-6361/202347801},
archivePrefix = {arXiv},
       eprint = {2309.08657},
 primaryClass = {astro-ph.SR},
       adsurl = {https://ui.adsabs.harvard.edu/abs/2023A&A...678L...3V},
      adsnote = {Provided by the SAO/NASA Astrophysics Data System}
}

