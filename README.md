# colpitts oscillator design
A colpitts oscillator at 187 MHz using ADS (Advanced Design System)
This is the colpitts oscillator circuit
![desgin](https://user-images.githubusercontent.com/47606879/142784825-169ed5eb-5390-446d-a61e-7ee9ff6fed6a.jpg)

KCL equations:
- (V_1- V_cc)/R_C   + g_m.V_π  +  (V_1-V_2)/R_B =0
- V_π/r_π +V_π.C_1.s+  (V_π-V_2)/(L.s)=0
- V_2.C_2.s+  (V_2-V_1)/R_B +  (V_2- V_π)/(L.s)=0

Matrix of equations: 
![mat](https://user-images.githubusercontent.com/47606879/142784953-074440e1-7d66-4abb-b7cf-84ff93eaa002.jpg)

Determinant of this matrix should be equal to zero in order to have osciallation.
- (1/R_B +1/R_C ).[(1/(L.s))^2-(1/r_π +C_1.s+1/(L.s)).(C_2.s+1/R_B +1/(L.s))]+(-1/R_B ).[(-1/R_B )(1/r_π +C_1.s+1/(L.s))+(1/(L.s)).g_m=0  
Both real part and imaginary part should be equal to zero: 
    - 〖w 〗^2=  ((β+1).R_C+ R_B+ r_π)/(L.(C_1  .R_B+ C_2  .(R_C+ r_π ) )
    - 〖w 〗^2≅((β+1).R_C)/(L.(C_1  .R_B+ C_2  .(R_C ) )=  ((β+1).R_C/R_B )/(L.(C_1  + C_2  .(R_C/R_B )) )  ≅  ((β+1))/(L.C_2 )  
    ---->  C_2.  R_C/R_B ≫ C_1    →  R_C> R_B
    - w^2=  1/(C_T.L)+  1/(〖C_1.C〗_2.r_π.(R_C+R_B)) 
    - 1/(〖C_1.C〗_2.r_π.(R_C+R_B ) )≪  1/(C_T.L) 
          r_π.(R_C+R_B )≫10^6
          r_π.(R_C+R_B )  ~ 10^8
          r_π~ 10^3
          (R_C+R_B )  ~ 10^5
          C_T=  〖C_1.C〗_2/〖C_1+C〗_2 
          w ≅  1/√(C_T.L)

## Choosing Caacitors and Reluctance for f = 187 MHz
L=1μH
w=2π.f ,L →C_T=0.72436 pF
n=0.04
C_2=18.109 pF
C_1=0.7545 pF

## V1
### - 0 - 200 nsec
  ![image](https://user-images.githubusercontent.com/47606879/142785292-5ee590de-f4c9-42f3-bebc-54afac811ac8.png)
  
### - 0 - 1 micro sec
  ![image](https://user-images.githubusercontent.com/47606879/142785336-fff99601-d5fa-4bb6-8cf0-3b3e4d251282.png)

### - Harmonics
  ![image](https://user-images.githubusercontent.com/47606879/142785344-17a82041-8d43-486f-8a38-e3a49ccb241a.png)

## Vout
### - 0 - 200 nsec
  ![image](https://user-images.githubusercontent.com/47606879/142785412-0d77e280-e56b-4439-b348-2c8e876f0949.png)

### - 0 - 1 micro sec
  ![image](https://user-images.githubusercontent.com/47606879/142785433-d9d2c672-97dd-4f3b-85a0-3bb6f53ced82.png)

### - Harmonics
  ![image](https://user-images.githubusercontent.com/47606879/142785446-8e537427-72b9-4bcb-9f16-7d6ab179f2d4.png)



This oscillator works perfectly at 187 MHz


 
  
  
  
  
  
  
  
  
  
  
  
  
 
 
 

 





 
