Diagnosing submesoscale mode water formation in eNATL60
=======================================================


We provide the notebooks in which we calculate the submesoscale potential vorticity flux terms `Mode-water_Jfluxes.ipynb <Mode-water_Jfluxes.ipynb>`_ via the parametrization proposed by `Wenegrat et al. (2013) <https://journals.ametsoc.org/doi/full/10.1175/JPO-D-17-0219.1>`_ to diagnose the relative contribution of surface forcing on mode water formation in the Gulf Stream region.
The tidally-forced North Atlantic simulation (eNATL60) we analyze has the horizontal resolution of 1/60 with 300 vertical layers, which allows for well formed mesoscale eddies and partially resolves the submesoscales.
The results are plotted in `Jflux_outputs.ipynb <Jflux_outputs.ipynb>`_.

We demonstrate that, by taking advantage of the `Pangeo architecture <http://pangeo.io/>`_, we can analyze the dataset of eNATL60 hosted on Occigen at CINES, the French national supercomputing facility, directly on Occigen using its computational nodes. 
This workflow eliminates the bottleneck of having to transfer and store a copy of the data on another cluster for analysis.
The Pangeo architecture, based on Python and Jupyter, allows the user to:

- Focus on the science, rather than having to spend time on setting up the environment.
- Move fluidly between prototyping the code and deploying it operationally for analysis.

The lapse time of analyzing each hourly output took less than two minutes, which resulted in going through each daily file in ~30 minutes.
The conda environment used in this analysis was packaged via `conda-pack <https://conda.github.io/conda-pack/>`_ and is listed in the file `spec-file.txt <spec-file.txt>`_. 

Acknowledgements:
-----------------
The full three-dimensional dataset used for this analysis is unfortunately too large to host on a Binder cluster but the two-dimensional data of sea-surface height and horizontal velocity are available on `Pangeo <https://catalog.pangeo.io/browse/master/ocean/MEOM_NEMO/>`_.

The eNATL60 twin-experiment (with and without tidal forcing) is the result of a collaboration between `Ocean Next <http://www.ocean-next.fr/>`_ and the `MEOM group <https://meom-group.github.io/>`_ at `IGE <http://www.ige-grenoble.fr/>`_.
eNATL60 experiments have been performed on the `MareNostrum IV supercomputer (Barcelona, Spain) <https://www.bsc.es/>`_ thanks to a 40 million cpu-hour allocation granted by `PRACE <https://prace-ri.eu/>`_: project ReSuMPTiOn, call #16. 
The complete eNATL60 output data archive (~ 1.5 PB) is hosted at `CINES (Montpellier, France) <https://www.cines.fr/>`_. Uchida acknowledges additional support from the French Make Our Planet Great Again (MOPGA) initiative.


