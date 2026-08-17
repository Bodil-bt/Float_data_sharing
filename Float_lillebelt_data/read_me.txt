Argo Lillebaelt tethering-float data.

Profile_Data contains per-station data (time at surface, lon, lat, connection
(1/0)). Data contains every sensor sample at depth.

The two files link on "Profile": Profile==1 is the same station in Data and
Profile_Data. Different deployments are distinguished by "Deployment_no": [4 5 7 8].
Deployment 8 is the SGAV nke-PFV2 float (deployed June 2026), continuing the
tethering deployments started April 2025 at the same site (deployments 4,5,7)
with the first small float; its Profile_no continues that numbering.

"Stage" in Data marks the float phase: descending=190, drifting/parking=290,
ascending=590, >600 = surface measurements. So bottom (park) data can be taken
as Stage==290 (optionally with a depth filter, e.g. PRES>22 dbar).

Oxygen: DO_mgL (mg/L), DO_umolKg (umol/kg), DO_sat (% saturation); AOU and pO2
are derived. PRES = pressure (dbar); Depth = metric depth (m, positive down,
from PRES via TEOS-10 gsw_z_from_p). rho = in-situ density.

Data quality: from ~11 Dec 2025 until the float was recovered (end of that
deployment) the CTD pump stalled, corrupting salinity. PSAL and all salinity-
derived fields (rho, DO_umolKg, DO_mgL, DO_sat, AOU, pO2) are NaN in that
window; temperature (TEMP), pressure (PRES) and Depth are unaffected.
