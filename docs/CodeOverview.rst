*************
Code Overview
*************

The UPP can be used to post-process WRF-ARW, WRF-NMM, NMMB, GFS, CFS, and FV3 forecasts with current
support within UFS applications available for FV3 only. It can ingest FV3 write component files in
netCDF and binarynemsiompiio format.

UPP Functionalities:

   -  Interpolates the forecasts from the models native vertical coordinate to NWS standard output
      levels (e.g., pressure, height) and computes mean sea level pressure. If the requested parameter
      is on a models native level, then no vertical interpolation is performed.

   -  Computes diagnostic output quantities (e.g., convective available potential energy, helicity,
      relative humidity). A full list of fields that can be generated by the UPP is provided in
      :doc:`UPP_GRIB2_Table`.

   -  Outputs the results in NWS and WMO standard GRIB2 format (see
      `Grib documentation <http://www.nco.ncep.noaa.gov/pmb/docs/>`_).
