# Bathymetry Gradient Analysis

This project identifies abrupt shallow-to-deep bathymetric transitions in the GEBCO 2023 DEM. The initial study focuses on the Azores and Cape Verde because both combine exposed land with nearby abyssal depths, allowing steep transitions to be traced from approximately sea level rather than from an offshore continental shelf break.

The analysis is intended as a general method for locating unusually steep submarine slopes over short horizontal distances. Potential applications include identifying areas susceptible to turbidity currents and other gravity flows, assessing terrain hazards to submarine cable networks ([Submarine Cable Map](https://www.submarinecablemap.com)), and supporting future mapping of seafloor faults or fractures. The same approach could also be applied to infrastructure-risk studies in areas such as the Norwegian Trench, including submarine pipelines.

## Current workflow

1. Calculate geodetically corrected seafloor slope from the DEM.
2. Coarsen and smooth each region, then identify discrete shallow sources at sea level or within a 330 ft proxy tolerance for unresolved rocky outcrops.
3. Find the shortest route from each source to the -z ft contour, rank candidates by average slope, and retain the top three.
4. Expand each route into a continuous ramp surface using local downslope direction, slope support, and gap filling.
5. Plot ramp surfaces, start points, regional depth maxima, island outlines, and summary statistics in 2D Matplotlib and interactive 3D Plotly views.

InterRidge hydrothermal vent data is also loaded for regional comparison and continued work

<img src="./images/area_of_interest_formigas_hole.png"
     alt="Formigas Hole area of interest"
     width="700">

**Data:** GEBCO 2023 bathymetry and InterRidge Hydrothermal Vents Database v3.4.
