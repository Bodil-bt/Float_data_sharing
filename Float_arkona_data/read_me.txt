Baltic PROVOR float 4903784 - CTD + oxygen + chlorophyll + backscatter +
irradiance (Baltic Sea, Bornholm Basin, ~55 N). This float is retired; this is a
one-time snapshot of the DTU-processed (delayed-mode) product.

Two files:
  Profile_Data.csv - one row per profile (descent 190 / ascent 590): surface time,
                     position, MLD, sun angle, and Kd per wavelength.
  Data.csv         - every sample at depth, including the park/bottom phase.

Link the two files on "Profile" (the Argo cycle number); "Stage" tells the phase
apart: descending=190, drifting/parking(near bottom)=290, ascending=590. The park
rows (290) give bottom-water properties; they have no separate Profile_Data row.

Columns in Data.csv:
  Profile, Profile_no - Argo cycle number / sequential id
  Stage               - 190 descent, 290 park/bottom, 590 ascent
  Datetime            - profile date/time (UTC)
  PRES, Depth         - pressure (dbar) and metric depth (m, +down, gsw)
  TEMP, PSAL          - temperature (degC), practical salinity
  DO_umolKg, DO_mgL   - dissolved oxygen (optode-adjusted; umol/kg and mg/L)
  Chla                - chlorophyll-a (mg/m^3; corrected fluorescence)
  BScat               - backscatter (m^-1)
  Ed380/443/490/555   - downwelling irradiance at 380/443/490/555 nm, DARK-
                        CORRECTED and quality-controlled per the DTU light
                        processing (dark offset removed, poly-4 log-fit QC).
                        UNITS: sensor counts (relative, dark-corrected) - NOT
                        calibrated physical irradiance. Use for profile shape /
                        the Kd fit; the calibrated light product is Kd below.
                        Blank where flagged, at night, or in the dark park phase.

Columns in Profile_Data.csv:
  Profile, Profile_no, Stage, Datetime, Latitude, Longitude, MLD, Sun_angle,
  Kd380/443/490/555 - diffuse attenuation coefficient (m^-1) per wavelength, from
                      a log-linear fit of the corrected irradiance within the ML.

Density, depth and MLD use GSW / TEOS-10. Empty cells = no valid value at that
level for that variable.
