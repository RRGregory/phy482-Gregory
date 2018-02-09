In circular particle accelerators, the particles are confined to circular orbits with strong focusing quadrupole magnets. The quadrupole magnets exert a linear restoring force on the particles. A quadrupole magnet will focus a beam of particles in the horizontal plane and defocus the beam in the vertical plane, or vice versa. To compensate for this, accelerator rings have a series of alternating focusing and defocusing quadruple magnets that have a net focusing effect on the beam[1]. For this reason, these kinds of accelerators are also referred to as alternating gradient machines. Alternating gradient machines are used because the mean deviation of the synchronous orbit from the ideal orbit is much smaller in an alternating gradient machine than in a constant gradient machine[2].

This magnetic focusing is illustrated by this gif[3]![qpole](https://nagysandor.eu/AsimovTeka/tevatron_hu/images/agfocus.gif)

This image shows the magnetic fields of alternating gradient quadrupoles. In order to change the gradient of the magnet, the north and south poles are switched. The blue dots represent particles passing through the magnetic field. As the animation shows, the particles get repeatedly focused and unfocused in the vertical and horizontal axes.

![realqpole](http://news.fnal.gov/wp-content/uploads/2013/07/HQO2-coil-medres.jpg)

This is an image of a real-life quadrupole magnet. This magnet is called HQ02a, and was developed at Fermilab.

These quadrupole magnets go inside circular particle accelerators, such as the CERN Super Proton Synchrotron, pictured below.[4]

![sps](https://home.cern/sites/home.web.cern.ch/files/image/accelerator/2013/01/sps.jpg)

The equations of motion of the particles in an accelerator can be described with a linear approximation. This can be done using the following curvilinear coordinates[2]:

$s = $ the distance along the equilibrium orbit measured from some fixed reference point to that point on the orbit closest to the point $P$.

$x = $ the horizontal component of the displacement of $P$ from the equilibrium orbit (taken to be positive in the outward direction)

$z = $ the vertical component of the displacement

The equations of motion for a particle in orbit are:

$$\frac{d^2x}{ds^2} = -\frac{1-n(s)}{\rho^2(s)}x$$

$$\frac{d^2z}{ds^2} = -\frac{n(s)}{\rho^2(s)}z$$

Where $n$ is the field gradient index, defined as

$$n=-\frac{r}{B}\frac{\partial B}{\partial r}$$

$\rho(s)$ is the radius of curvature of the equilibrium orbit at $s$, defined as

$$\rho(s) = \frac{pc}{eB_z (s,0,0)}$$

and $n(s)$ is the field gradient at $s$ defined as

$$n(s) = - \frac{\rho^2}{pc/e} \frac{\partial B_z}{\partial x}$$

These equations of motion are periodic and satisfy Hill's equation. The equations of motion are generally non-linear, but in order to do a linear approximation one can keep only the lowest order terms of $x$ and $y$. Then, the equations of motion can be written in the form:

$$\frac{d^2y}{ds^2} = -K(s)y$$

where $y$ is the horizontal or vertical displacement, where $K$ satisfies: $K(s+L) = K(s)$ and $L=\frac{C}{N}$ where $C$ is the circumference of the particle's orbit, and $N$ is a number of identical sections or "unit cells" in the synchrotron.

In an accelerator, $K$ is usually constant by design, so only constant values of $K$ will be considered in finding solutions to the equations of motion. If you solve this linear second order differential equation for the case of $K$ being a positive constant and put it in matrix form you get:

$$
\left(\begin{array}{cc}
y \\
y'
\end{array}\right)_0
\left(\begin{array}{cc}
cos(\sqrt{K}l) & \frac{sin(\sqrt{K}l)}{\sqrt{K}} \\
-\sqrt{K}sin(\sqrt{K}l) & cos(\sqrt{K}l)
\end{array}\right)=
\left(\begin{array}{cc}
y \\
y'
\end{array}\right)
$$

for some distance $l$. If $K$ is negative you get the matrix:

$$
\left(\begin{array}{cc}
y \\
y'
\end{array}\right)_0
\left(\begin{array}{cc}
cosh(\sqrt{K}l) & -\frac{sinh(\sqrt{|K|}l)}{\sqrt{|K|}} \\
-\sqrt{|K|}sinh(\sqrt{|K|}l) & cosh(\sqrt{K}l)
\end{array}\right)=
\left(\begin{array}{cc}
y \\
y'
\end{array}\right)
$$

Or for the simplest case in which $K=0$, the matrix is:

$$
\left(\begin{array}{cc}
y \\
y'
\end{array}\right)_0
\left(\begin{array}{cc}
1 & l \\
0 & 1
\end{array}\right)=
\left(\begin{array}{cc}
y \\
y'
\end{array}\right)
$$

These first two solutions describe the oscillatory motions of a particle as it goes through the focusing and defocusing magnets. The third matrix corresponding to $K=0$ describes the particle's motion as it goes through the drift space between magnets.

These matrices can be defined as[5]:

$$
M_+ = \left(\begin{array}{cc}
cos(\sqrt{K}l) & \frac{sin(\sqrt{K}l)}{\sqrt{K}} \\
-\sqrt{K}sin(\sqrt{K}l) & cos(\sqrt{K}l)
\end{array}\right)
$$

$$
M_- = \left(\begin{array}{cc}
cosh(\sqrt{K}l) & -\frac{sinh(\sqrt{|K|}l)}{\sqrt{|K|}} \\
-\sqrt{|K|}sinh(\sqrt{|K|}l) & cosh(\sqrt{K}l)
\end{array}\right)
$$

and $M = M_+M_-$

a "period" can be considered as one focusing and defocusing sector, then the values of $y$ and $y'$ at the end of a period can be written as a function of the values of $y$ and $y'$ at the beginning of a period:

$$
\left(\begin{array}{cc}
y
y'
\end{array}\right)_t = M_+M_-
\left(\begin{array}{cc}
y \\
y'
\end{array}\right)_0 = M
\left(\begin{array}{cc}
y \\
y'
\end{array}\right)_0
$$

These matrices are encountered repeatedly and represent the motion of the particles all the way around the accelerator. The image below shows a schematic representation of the effects of alternating gradient magnets. The blue lines represent approximate particle trajectories. The section below the blue band that says "cell" is one repeated "unit cell"[6].

![fodo](https://github.com/RRGregory/phy482-Gregory/blob/master/FODO.png)

We can then define a value $cos(\mu) = (1/2)Tr(M)$ where $Tr(M)$ is the trace of the matrix $M$. By doing some matrix algebra, it is shown that the condition for the particle motion to be stable is that $|cos(\mu)| < 1$. Physically, $\mu$ represents the phase change of betatron oscillation as a particle goes through a magnet cell. The region of stability can be represented graphically by introducing values for the magnetic index, $n_1$ and $n_2$. The figure below shows the region of stability for radial and vertical oscillations.[5]

![st](https://github.com/RRGregory/phy482-Gregory/blob/master/region_of_stability.png)


References

1. Holzer, B.J. "Introduction to Particle Accelerators and their Limitations" May 2017. CERN. 10.5170/CERN-2016-001.29

2. E.D. Courant and H.S. Snyder. 1958. "Theory of the Alternating Gradient Synchrotron." Ann. Phys. 3, 1-48.

3. Malamud, Ernie. _Fermilab's Chain of Accelerators Accelerator Details:  How Synchrotrons Work_, August 16, 2000 https://nagysandor.eu/AsimovTeka/tevatron_hu/synchrotrons.html

4. "sps.jpg". 2012. CERN.

5. E. Regenstreif. 1959. "The CERN Proton Synchrotron, Part 1". (CERN 59-29) Proton Synchrotron Division. CERN European Organization for Nuclear Research. Geneva. 5-41

6. Gregory, RuthAnn. "FODO Lattice". February 7 2018 https://github.com/RRGregory/phy482-Gregory/blob/master/FODO.png
