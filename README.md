I am interested in detecting large bathymetric transitions occurring across limited horizontal distances

In the Formigas example image, the important signal is something like:
relatively shallow seafloor -> several thousand feet deeper within perhaps a couple nautical miles


## Bathymetric gradient

The bathymetric gradient magnitude describes the rate of change of seafloor elevation with horizontal distance:

```math
|\nabla z|
=
\sqrt{
\left(\frac{\partial z}{\partial x}\right)^2
+
\left(\frac{\partial z}{\partial y}\right)^2
}
```

where $z$ is seafloor elevation and $x$ and $y$ are horizontal coordinates.

The corresponding seafloor slope angle is:

```math
\theta
=
\tan^{-1}\left(|\nabla z|\right)
```

or, in degrees,

```math
\theta_{\mathrm{deg}}
=
\frac{180}{\pi}
\tan^{-1}\left(|\nabla z|\right)
```

<img src="./images/area_of_interest_formigas_hole.png"
     alt="Formigas Hole area of interest"
     width="700">

