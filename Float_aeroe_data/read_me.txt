SGAV_provor float - reduced CTD + oxygen data (Aeroe).

Profile_Data contains per-station data (surface time, lon, lat). Data
contains every CTD/oxygen sample at depth.

The two files link on "Profile": Profile==X is the same station in both.

"Stage" in Data marks the float phase: descending=190, drifting/parking=290,
ascending=590, >600 = surface. Bottom (park) data = Stage==290.

Columns: PRES = pressure (dbar); Depth = metric depth (m, positive down);
TEMP (degC); PSAL (practical salinity); DO_umolKg (umol/kg); DO_mgL (mg/L).
