# How does a neural network really work

Machine learning models are things that fit functions to data.

1. TOC
{:toc}

## Create a general quadratic function

The first step is that we create a general quadratic function $3x^2 + 2x + 1$ and plot it:
![](/images/function.png "plot $3x^2 + 2x + 1$")

## Fit the function manually

The second step is to create some data match the function but with noise.
![](/images/data.png "data with noises")
And we try to adjust the a, b, c manually to find a curve that matches the data to reconstruct the function:
![](/images/data1.png "adjust coefficients manually")

## Loss function

Loss function is the measurement of how good is our model. When we adjust the coefficients, loss function helps us check whether it is better or worse.

Loss function mse (mean square error):
![](/images/lossfunction.png "Loss function mse")

Add a MSE to indicate how good our curve is when we adjust coefficients:
![](/images/loss.png)

Now we have a number, so we can adjust coefficients manually. And a faster way is to calculate its derivative or gradient. Which can tells if you increase the input, how much does the output increase or decrease. The code is shown in following images:
![](/images/gradient1.png)
![](/images/gradient2.png)
![](/images/gradient3.png)
The output of abc.grad tells us that increase a,b,c will decrease the loss, which means the curve is better. Also, increasing a can decrease the loss faster because 10.9887 is biggest.
So we decrease a, b, c a little bit to see whether the loss is smaller than 11.4648.
![](/images/gradient4.png)
Loss decreases to 10.11 as expected. If we do it several times:
![](/images/gradient5.png)
The loss keeps improving. This is called optimization.

## Mathematical function

The last step is what mathematical function should be used to find parameters. The quadratic is too simple to represent relationship between parameters and pixels.
(To be continued..)