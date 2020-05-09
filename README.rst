Diagnosing submesoscale mode water formation in eNATL60
=======================================================


We provide the notebooks in which we calculate the submesoscale potential vorticity flux terms `Mode-water_Jfluxes.ipynb <Mode-water_Jfluxes.ipynb>`_ via the parametrization proposed by `Wenegrat et al. (2013) <https://journals.ametsoc.org/doi/full/10.1175/JPO-D-17-0219.1>`_ to diagnose the relative contribution of surface forcing on mode water formation in the Gulf Stream region. The results are plotted in `Jflux_outputs.ipynb <Jflux_outputs.ipynb>`_.

We demonstrate that by taking advantage of the `Pangeo architecture <http://pangeo.io/>`_, we can analyze the dataset of eNATL60 hosted on Occigen at CINES, the French national supercomputing facility, directly on Occigen using its computational nodes. This workflow eliminates the bottleneck of having to transfer and store a copy of the data on another cluster for analysis. The conda environment used in this analysis was packaged via `conda-pack <https://conda.github.io/conda-pack/>`_ and is listed in the file `spec-file.txt <spec-file.txt>`_. 

The full three-dimensional dataset used for this analysis is unfortunately too large to host on a Binder cluster but the sea-surface data are available on `Pangeo <https://catalog.pangeo.io/browse/master/ocean/MEOM_NEMO/>`_.



