## Index
![dark](https://user-images.githubusercontent.com/12748752/126882595-d1f5449e-14bb-4ab3-809c-292caf0858a1.png)

### The Curve 

<p align="center" ><img src="https://user-images.githubusercontent.com/12748752/186566132-7e8711f4-21ba-41dc-870f-d350c8916830.png" width=30%/>
<br><ins><b>Sinusoidal Curve</b></ins></p>

This green curve is a **Sinusoidal Curve**, from which we draw the followings-
* Some **data points** at some specific intervals, 
* And we just add some **noise** to this dataset which is given by the **blue dot** or **blue circles**.

### Fitting
<p align="center"> <img src="https://user-images.githubusercontent.com/12748752/186587311-d3080729-7d9a-4882-9d9b-88e6aac49cab.png" width=30% />
<br><ins><b>Sum-of-squares Error Function</b></ins></p>


So the idea here is, we want to fit into a polynomial and to vary the degree of the polynomial and see how the fix look like. We fit them by using an error term to perform the regression with **least squared error**

$$\large{\color{Purple} \sum_{i=1}^{m} \Bigl(y^{(i)}- \hat{y}^{(i)} \Bigl)^2}$$ 

$$\large or$$

$$\large{\color{Purple} \sum_{i=1}^{m} \Bigl( t^{(i)} -y(x^{(i)};w) \Bigl)^2}$$

So **_t_** is the ground truth or the correct answer and whatever your polynomial outputs, and it is given by **_y_**, so your error is basically what you are going to use,

### 0<sup>th</sup> Order, 1<sup>st</sup>Order & 3<sup>rd</sup> Order Polynomials

<img src="https://user-images.githubusercontent.com/12748752/186598693-db686c38-6e19-4cf5-82ca-efef4a1e2fe2.png" />

So, at the extreme left we have a **zero degree polynomial**, which is nothing but a **constant term**, so as you can see there is a red line, which is actually the fit, the fitted curve, of course does not match the data that we have used.

At the middle we use a **first degree polynomial**, which is nothing but a **linear fit**, and did not fit

At the right we have **third degree polynomial**. 


### 9<sup>th</sup> Order Polynomials
<p align="center"> <img src="https://user-images.githubusercontent.com/12748752/186589809-16614600-9242-48a5-9841-900db3964731.png" width=30% />
<br><ins><b>9<sup>th</sup> Order Polynomials</b></ins></p>


 
So ideally when you are done with the fit, you would expect the **red curve** to _lie close_ to the **green curve**, but in this case, _in between samples is actually off_. 

So **even the with higher degree polynomial is, we are able to fit every point exactly**, so that our **fitting error is very small**. We see that in points, other than the blue circles, it is actually **quite far from the ground truth**.

### Over fitting
<p align="center"> <img src="https://user-images.githubusercontent.com/12748752/186604933-a349fff4-9c77-49db-8bc6-512eb5e2b9d2.png" width=35%/>
 <br><ins><b>Graphs of the <i>Root-Mean-Square Error</i>, evaluated on the <i>training set</i> and on an independent <i>test set</i> for various values of <i>M</i></b></ins></p>

So, if we actually plot the error, the error as we defined previously, so as you fit the error 4 different values of **M** that is degree of the polynomial, see that as we hit the higher degree polynomials, the error on the **training data is very small**, which is what the blue circle indicates. However the test data error, this starts to diverge. So, this phenomenon is referred to as overshooting. Similarly has become back here, we see that again, there is quite high when we are using a polynomial of degree zero, that is we are just fitting it to a constant function. So in both the cases, we have a fairly large error, one in this end of the spectrum, we can call this under fitting and at this end of the spectrum, we will call it **over fitting**.

<p align="center" ><img src="https://user-images.githubusercontent.com/12748752/186613543-48161972-0869-43d6-a0d2-7cb6807132dd.png" width=30%/></p>

## Bias Variance trade off
![light](https://user-images.githubusercontent.com/12748752/126882596-b9ba4645-7001-435e-9a3c-d4416a2543c1.png)

<img src="https://user-images.githubusercontent.com/12748752/186632648-5b374274-5a53-40ac-9bd7-1cc6e9043094.png" width=20% align="right"/>

* **Bias Variance trade off** relates to **model complexity** which is nothing but the number of parameters and the basis functions (<img src="https://latex.codecogs.com/svg.image?\large{\color{Purple}&space;x,&space;x^2,&space;\cdots,&space;x^m}" title="https://latex.codecogs.com/svg.image?\large{\color{Purple} x, x^2, \cdots, x^m}" align="center"/>) used in the model.
*  $\hat{Y}$  is what is called a statistical estimate of the true model 𝑌

#### Bias:
Expectation value of the difference between the model prediction and the correct value. Here the expectation is over the X and different data sets.

$$ \large{\color{Purple}\mathbf{Bias^2} = E \\{[\hat{Y} -Y ]^2 \\} }$$  
  
#### Variance:  
The variance is the variance on the predictions of the model trained using different data sets. 

$$ \large{\color{Purple}\mathbf{Variance} = E \\{[\hat{Y} - \bar{\hat{Y}} ]^2 \\} } $$

<p align="center"> <img src="https://user-images.githubusercontent.com/12748752/186631445-9d8bf8b3-3d10-47dc-9fc6-6fbaf6caf232.png" width=30% />
<br><ins><b>Bias Variance trade off graph</b></ins></p>

#### Model Complexity on Bias Variance
* Complex models with many parameters might  have a small bias but large variance. 
* Simple models with few parameters might have a large bias but small variance.

<p align="center"> <img src="https://user-images.githubusercontent.com/12748752/186634193-9a9ed2a1-e146-4e8f-8d20-ed2b28f6b04d.png" width=60% />
<br><ins><b>Bias Variance trade off graph</b></ins></p>

<img src="https://user-images.githubusercontent.com/12748752/186638585-b1af972f-00d6-4901-8c5a-1e3ea24bc59f.png" width=80%/>

### How to measure Bias-Variance?
![light](https://user-images.githubusercontent.com/12748752/126882596-b9ba4645-7001-435e-9a3c-d4416a2543c1.png)






