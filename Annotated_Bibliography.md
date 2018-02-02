    1. Holzer, B.J. "Introduction to Particle Accelerators and their Limitations" May 2017. CERN. 10.5170/CERN-2016-001.29

Summary:

This paper describes the limitations of particle accelerators while explaining some of the physics concepts behind how these accelerators work. One such physical limit that is relevant to electricity and magnetism is an accelerator's magnetic guide field. The paper briefly describes how dipole magnets bend the charged particles to make them stay in orbit around the accelerator. The paper focuses more on the quadrupole magnets that focus the beam, and keep the particles closer together.

The quadrupole magnets exert a linear restoring force on the particles. Due to the orientation of the magnetic field lines and Maxwell's equations, a dipole magnet will focus a beam of particles in the horizontal plane and defocus the beam in the vertical plane, or vice versa. To compensate for this, accelerator rings have a series of alternating focusing and defocusing quadruple magnets that have a net focusing effect on the beam. See Figure 14 in the paper for a diagram of the magnetic fields of a quadruple magnet.



    2. E.D. Courant, M.S. Livingston, and H.S. Snyder. 1952. "The Strong Focusing Synchrotron - A New High Energy Accelerator." The Physical Review, 88: 1190-1196.

Summary:

This paper goes into more details about strong focusing. In synchrotrons (and other accelerators) some of the particles will deviate from their design trajectories due to the energy spread in the injected beam, scattering by residual gas, magnetic inhomogeneities, or frequency errors. These deviations are oscillatory and the paper mathematically describes the amplitudes, frequencies, and relative stabilities of these oscillations. However, I am more interested in focusing (no pun intended) on the corrections for these oscillations, one of which is strong focusing.

Strong focusing uses quadrupole magnets of alternating gradients to focus particle beams kind of like a series of lenses. A quadrupole magnet used in a synchrotron has a doubly-divergent magnetic field with uniform and equal values of dBz/dy and dBy/dz with the center of the magnet on the x axis. The pole faces of the magnet are shaped like rectangular hyperbolas. In a strong focusing lens, there would be two of these magnets separated by some length and rotated 90 degrees relative to each other.



    3. E.D. Courant and H.S. Snyder. 1958. "Theory of the Alternating Gradient Synchrotron." Ann. Phys. 3, 1-48.
    
Summary:

This paper defines a value $n$ known as the field gradient index, defined as 

$$n=-\frac{r}{B}\frac{\partial B}{\partial r}$$ 

In alternating-gradient synchrotrons, the value of $n$ is varied between large positive and negative values to obtain strong focusing forces. This paper defines the following curvilinear coordinates:

$s = $ the distance along the equilibrium orbit measured from some fixed reference point to that point on the orbit closest to the point $P$.

$x = $ the horizontal component of the displacement of $P$ from the equilibrium orbit (taken to be positive in the outward direction)

$z = $ the vertical component of the displacement

The equations of motion for a particle in orbit are:

$$\frac{d^2x}{ds^2} = -\frac{1-n(s)}{\rho^2(s)}x$$

$$\frac{d^2z}{ds^2} = -\frac{n(s)}{\rho^2y(s)}z$$

where 

$$\rho(s) = \frac{pc}{eB_z (s,0,0)}$$ is the radius of curvature of the equilibrium orbit at $s$ and $$n(s) = - \frac{\rho^2}{pc/e} \frac{\partial B_z}{\partial x}$$

These equations of motion are periodic and satisfy Hill's equation. This paper then writes those equations in the form: 

$$\frac{d^2y}{ds^2} = -K(s)y$$ 

where $y$ is the horizontal or vertical displacement, where $K$ satisfies: $K(s+L) = K(s)$ and $L=\frac{C}{N}$ where $C$ is the circumference of the particle's orbit, and $N$ is a number of identical sections or "unit cells" in the synchrotron.

Now, if you solve this linear second order differential equation for the case of $K$ being a positive constant and put it in matrix form you get:

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

for some ditance $l$. If $K$ is negative you get the matrix: 

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

These first two soulutions describe the oscillatory motions of a particle as it goes through the focusing and defocusing magnets. The third matrix corresponding to $K=0$ describes the particle's motion as it goes through the drift space between magnets.



    4. E. Regenstreif. 1959. "The CERN Proton Synchrotron, Part 1". (CERN 59-29) Proton Synchrotron Division. CERN European Organization for Nuclear Research. Geneva. 5-41
 
Summary: 
 
In alternate gradient focusing, the circumference of a magnet is split into alternating sectors in which the field increases and decreases radially. A sector in which the magnetic field decreases radially outward will focus the beam in the horizontal plane, and defoucs the beam in the vertical plane. For a sector in which the magnetic field increases radially outward, the opposite will occur. A strong net focusing effect can be obtained if the sectors are apporpriately laid out. This is the principle behind alternating gradient accelerators. Alternating gradient machines are used because the mean deviation of the synchronous orbit from the ideal orbit is much smaller in an alternating gradient machine than in a constant gradient machine.

If we define the matricies:

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

and consider a "period" as being one focusing and defocusing sector, then the values of $y$ and $y'$ at the end of a period can be written as a function of the values of $y$ and $y'$ at the beggining of a period:

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

We can then define a value $cos(\mu) = (1/2)Tr(M)$ where $Tr(M)$ is the trace of the matrix $M$. By doing some matrix algebra, it is shown that the condition for the particle motion to be stable is that $|cos(\mu)| < 1$.

The region of stability for radial and vertical oscillations is graphed in figure 1.7 of this paper.