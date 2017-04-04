# load elevatr
library(elevatr)
library(sp)
library(raster)

# get example data
data("pt_df")
pt_df
data("lake")
plot(lake)

# use points to get point elevations
ll_wgs84 <- "+proj=longlat +ellps=WGS84 +datum=WGS84 +no_defs"
pt_df_elev <- get_elev_point(pt_df, prj = ll_wgs84 )
data.frame(pt_df_elev)

# use lake to get raster DEM
sunapee_dem <- get_elev_raster(lake, z = 12, src = "aws")
sunapee_dem
plot(sunapee_dem)
