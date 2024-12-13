# Initial Dilution
Initial Dilution (ID) is the reduction in concentration of a buoyant effluent as it rises from its discharge point to the water surface. 

# Key factors affecting dilution
|Parameter|Description|
|-|-
|Q|Volume flux of discharge m$^3/$s
|H|Water depth from outfall to free surface (m)
|$\rho_e$|density of effluent (kg/m$^3$)
|$\rho_a$|density of receiving water (kg/m$^3$)
|U|ambient current speed (m/s)

## Froude number
The *Froude number* is the ratio of a body's inertial to gravitational forces:
$$F_r=\frac{u}{\sqrt{gL}}$$
where $u$ is flow velocity, $g$ is gravitational acceleration and $L$ is a characteristic length. 

It is related to the *Richardson number* which is the ratio of potential to gravitational energy quantifies the effect of buoyancy on flow stability:
$$Ri = \frac{gH}{U^2}=\frac{1}{Fr^2}$$

The densimetric Froude number is:
$$F_r=\frac{u}{\sqrt{g'L}}$$
where $g'$ is the reduced gravity:
$$g'=g\frac{\rho_a-\rho_e}{\rho_a}$$

## Cederwall Equation:
This expression for initial dilution applies to low momentum jets where $F<1$. 

$$S=0.54F\left[\left(\frac{0.38H}{DF}\right)+0.66\right]^{\frac{5}{3}}$$

Modern outfalls are designed to discharge at $F>1$ (to avoid ingress of seawater at the outfall port) and the WRc equations are more appropriate.

## WRc Equations

*Note: WRc document introduces parameter $B=Q\rho_rg$. However, dilution equation (near-field) includes both $B$ and $Q$ which obscures dependence of flow rate on dilution. So equations below written without $B$*

Two regimes:
* **Buoyancy Dominated Near Field** (BDNF), where plume's behavoir primarily determined by its buoyancy. Here, the dilution depends on the relative density of the effluent but not the ambient current speed of the receiving water. 
*  **Buoyancy Domainated Far Field** (BDFF), where vertical velocity induced by buoyancy has decayed to less than that of the ambient current. The dilution depends on the magnitude of the ambient current, but not the relative density.



The cutoff between these two regimes is given by:

$$\frac{5Q\rho_rg}{HU^3}=\begin{cases}
\ge1&\textrm{Near-field}
\\
<1&\textrm{Far-field}
\end{cases}
$$

where $\rho_r=\frac{\rho_a-\rho_e}{\rho_a}$

The near-field regime then tends to apply at:
* high discharge rates
* shallow water depths
* low ambient current speeds

Consider fixed discharge rate, $Q$. At depth $H$, the critical speed is

$$U_c=\left(\frac{5Q\rho_rg}{H}\right)^{\frac{1}{3}}$$

If $U<U_c$, the flow regime is near-field; if $U>U_c$, the flow regime is far-field. 

As we move through the tidal cycle and $H$ varies, $U_c$ varies as well but to a much lesser extent due to the power exponent of $\frac{1}{3}$. 

At larger values of $H$ (high tide), $U_c$ is smaller, and the far-field regime applies at lower values of $U$. 

Similarly, $U_c$ increases slowly as the flow rate increases, meaning higher values of $U$ are required to activate the far-field regime.

For a given discharge depth $H$, the cutoff between the two regimes depends on the ratio $\frac{Q}{U^3}$. The near field regime corresponds to higher discharge rates and lower ambient current speeds. 

### Near-field
$$S=C_1\frac{B^{\frac{1}{3}}H^{\frac{5}{3}}}{Q}$$
$$S=C_1\frac{Q^{\frac{1}{3}}(\rho_rg)^{\frac{1}{3}}H^{\frac{5}{3}}}{Q}$$
$$S=C_1\frac{(\rho_rg)^{\frac{1}{3}}H^{\frac{5}{3}}}{Q^{\frac{2}{3}}}$$

Note that the near-field dilution is independent of $U$. 
An effluent with discharge concentration $C_0$ will dilute to:
$$C=\frac{C_0}{S}=\frac{C_0Q^{\frac{2}{3}}}{C_1(\rho_rg)^{\frac{1}{3}}H^{\frac{5}{3}}}$$

If the discharge flow rate is halved resulting in the effluent concentration doubling, the concentration after dilution becomes:
$$C=\frac{2C_0}{S}=\frac{2C_0\left(\frac{Q}{2}\right)^{\frac{2}{3}}}{C_1(\rho_rg)^{\frac{1}{3}}H^{\frac{5}{3}}}=\frac{2^{\frac{1}{3}}C_0Q^{\frac{2}{3}}}{C_1(\rho_rg)^{\frac{1}{3}}H^{\frac{5}{3}}}$$

This is a factor $2^{\frac{1}{3}}$ higher which indicates that when discharging a load of pollutant, it is preferable to discharge a higher rate of lower concetration effluent i.e. pre-dilution is beneficial.  

### Far-field

$$S=C_2\frac{UH^2}{Q}$$

The far-field dilution is independent of the relative density $\rho_r$. 
Here, the dilution is inversely proportional to the discharge flow rate, $Q$. Halving this flow rate (doubling the discharge concentration) therefore makes no difference to the resulting concentration.

$$C=\frac{2C_0}{S}=\frac{2C_0\frac{Q}{2}}{C_2UH^2}=\frac{C_0Q}{C_2UH^2}$$

When discharging in far-field conditions, it is the load rather than the balance between flow rate and concentration that determines the resulting dilution. 

Dilution in the far-field is proportional to $U$ i.e. increases at the rate that $U$ increases. 

As a test, substitute critical $U_c$ into far-field dilution equation:
$$S=C_2\left(\frac{5Q\rho_rg}{H}\right)^{\frac{1}{3}}\left(\frac{H^2}{Q}\right)$$

$$S=C_25^{\frac{1}{3}}\frac{(\rho_rg)^{\frac{1}{3}}H^{\frac{5}{3}}}{Q^{\frac{2}{3}}}$$

This is the same as the near-field solution if $C_1=C_25^{\frac{1}{3}}$. In practice, WRc presented a number of values of $C$ derived from field data corresponding to 95% minimum values, median minimum values and mean minimum values. 

In our assessments, we adopt the approach used by the EA, namely using the median minimum values. In this case $C_1=C_2=0.27$. 

So there is a slight discontinuity at the near/far field boundary, but given the scatter in the field data and general uncertainty this is deemed acceptable!


## Summary

### Cederwell equation (low momentum discharge)
$$S=0.54F\left[\left(\frac{0.38H}{DF}\right)+0.66\right]$$

### WRc Equations

$$S=\begin{cases}
0.27\frac{(\rho_rg)^{\frac{1}{3}}H^{\frac{5}{3}}}{Q^{\frac{2}{3}}}&&
\frac{5Q\rho_rg}{HU^3}\ge1 & \textrm{(Near-field)}
\\
0.27\frac{UH^2}{Q}&&
\frac{5Q\rho_rg}{HU^3}<1 & \textrm{(Far-field)}
\end{cases}$$

SEPA's initial dilution standards (50x for trade / secondary-treated sewage effluent) are specified in terms of 5%ile, i.e. the value to be exceeded for 95% of the time. 

This can be checked by either evaluating ID over suitable time period (spring/neap cycle) and calculating the 5%ile dilution value, or by using the water depth at Mean Low Water Springs.