+++
author = "Arief Koesdwiady"
title = "Unmanned Aerial Vehicle Tracking Control"
tags = [
    "project",
]
+++

This project presents the application of a non-linear control technique, i.e., Invariance and Immersion (I&I), in trajectory tracking control, observer and adaptive control for quadrotor unmanned aerial vehicle (UAV).

###  I&I Trajectory Tracking Control
This method was first introduced by Astolfi in 2003. The idea of this method is based on the system immersion and manifold invariance concepts. The main objective is to stabilize the system by immersing the plant dynamics into a target dynamic with a desired behavior.

Quadrotor is categorized as an underactuated system (fewers actuators than the degress of freedom, i.e., 4 actuators and 6 DOF); therefore, a two-loop controller (inner and outer loop controllers) is introduced. In the outer loop, translational dynamics {{< iqi >}}\((x, y, z)\){{< /iqi >}} are controlled by a PD tracking control, which returns the desired attitude {{< iqi >}}\((\phi,\theta,\psi)\){{< /iqi >}}. These desired attitude then will be tracked by the I&I inner controller. The complete structure of the controller can be seen in the following figure:

{{< rawhtml >}}
<div style="text-align:center">
  <img src="/images/ii.png"/>
</div>
{{< /rawhtml >}}

The error dynamics of the quadrotor body angular velocity are given by:

{{< iqb >}}
\[\begin{align}\dot e_1 &= e_2\\
\dot e_2 &= F(x_2) +G\tau - \ddot x_{1_d}\end{align}
\]
{{< /iqb >}}

where the controller after applying the I&I technique is given as:
{{< iqb >}}
\[\begin{align}
\tau = (G^\top G)^{-1}G^\top(-\gamma z - F(x_2) -\mu e_2 + \ddot x_{1d})
\end{align}
\]
{{< /iqb >}}

The results of the positions and attitude angles tracking can be seen in the following figure:

{{< rawhtml >}}
<div style="text-align:center">
  <img src="/images/iires.png" width="75%" height="75%"/>
</div>
{{< /rawhtml >}}

Check out the following video to see the tracking performance:

{{< youtube jiwoLsKon-k >}}
{{< rawhtml >}}
<br>
<br>
{{< /rawhtml >}}

***

**N.B.** The details of the work, including the observer and adaptive control designs, can be seen in my [thesis](/files/msc.pdf).