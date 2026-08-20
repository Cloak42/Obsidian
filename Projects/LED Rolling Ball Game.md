---
tags:
  - code-project
  - electronics-project
---
---
GitHub Repository:(NOT CREATED YET)

---
## Intro/Concept
Using physics kinematics equations to reproduce a ball on a tilting surface using an IMU ([[IMU Tests]]) for angle input, and displaying the acceleration of the theoretical block using addressable LEDs ([[Addressable LED]])

inspired a bit by pong...?

---
## The initial idea
using an inclined slope system with a variable slope angel to produce an acceleration down the plane and then convert it into position values and feed it to an LED strip using an IMU to provide an angle for the slope

inclined plane FBD:
![[Pasted image 20260819010933.png|396]]

math to find the acceleration down the plane:
$$
\begin{gathered}
sin(\theta)=\frac{F_{down}}{F_{g}} \\\\
F_{down}=(F_g)(sin(\theta)) \\\\
F_{g}=Mg\\\\
F_{down}=M(A_{down})\\\\
A_{down}=g(sin(\theta))
\end{gathered}
$$
using kinematic equations to find the position values
$$
\begin{gathered}
\text{kinimatic equation:}\\
{\Delta}x=V_i(t)+\frac{1}{2}(A)T^2\\\\
V_i=0\\
A=A_{down}\\\\
{\Delta}x=\frac{1}{2}g(sin(\theta))T^2\\\\
{\Delta}x=x_f-x_i\\
x_i=0\\\\
x_f=\frac{1}{2}g(sin(\theta))T^2
\end{gathered}
$$
now we have an equation for the x position of something following the acceleration of an inclined slope with of theta given a time and value and the gravitational acceleration


## Rethinking the Idea
the "ball"(led thats on) should:
- start in the middle
- stop moving when the 

---
## Concept Drawings/Notes:

---
## File ledged

| File Name | File Description |
| --------- | ---------------- |
|           |                  |

---
## Component Guide

| Component name/number | Component type | Component use/assosiated part |
| --------------------- | -------------- | ----------------------------- |
|                       |                |                               |
|                       |                |                               |

---
## Results/ updates

---