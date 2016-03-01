# Assignment 1

Q1) In this question we were asked to use inversion method to sample polar coordinates(r,theta) inside the unit circle. For this purpose I calculated the CDF of the probability distribution of r, which gave me P(r) = r^2. From the inversion method I had to take the inverse of the function, P^(-1)(y) = y^(1/2). Uniformly getting y value and then taking its square root gave me the r values of the polar coordinates. For the theta value I used uniform random function of numpy library. Then I drew them on a figure. From the image below you can see the result, from 5000 sample points: 
![alt tag](https://github.com/metehandoyran/Assignment-1/blob/master/figure_1.png?raw=true) 

BONUS: For the bonus part related to the Q1, I added generic versions of the functions. For getting the direction in n-dimensions I used n-variate gaussian to get a vector(direction), and for radius (r) I used CDF, which increases exponentially (for n=2, P(r)=r^2, for n=3 P(r)=r^3,...). For n=3 dimensions I also plotted the figure below:
![alt tag](https://github.com/metehandoyran/Assignment-1/blob/master/figure_2.png?raw=true) 

Q2) For this question I used the methods I've written for the first question. From the polar coordinates I got points in unit 2-norm ball. By using rejection sampling (rejected samples are shown by the red crosses) I drew samples from the closed unit ball for p = 1.5, which are shown below: (Acceptance rate is *0.8714*)
![alt tag](https://github.com/metehandoyran/Assignment-1/blob/master/figure_3.png?raw=true) 
By using rejection sampling (rejected samples are shown by the red crosses) I drew samples from the closed unit ball for p = 0.7, which are shown below: (Acceptance rate is *0.4055*)
![alt tag](https://github.com/metehandoyran/Assignment-1/blob/master/figure_4.png?raw=true)

For an alternative proposal I sampled from the 1-norm closed unit ball. For doing this I first got u and v coordinates from a coordinate axis which is 45 degrees different from the x-y coordinates. Then I calculated the arc tangent of the u/v, then translated the angle to x-y coordinates. Acceptance rate increased drastically, which became *0.6448* from *0.4055*. You can see the new proposed sampling below: 
![alt tag](https://github.com/metehandoyran/Assignment-1/blob/master/figure_5.png?raw=true)
