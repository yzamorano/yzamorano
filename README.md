The system does not correctly calculate the CDF of a Binomial using the Regularized Incomplete Beta for p=0.5.
restart;
n := 10;
f := x -> int(t^(n - x - 1)*(1 - t)^x, t = 0 .. 1 - p)/Beta(n - x, x + 1);
p := 0.5;
e := plot(f(x), x = 0 .. 10);
![BUG Maple](https://user-images.githubusercontent.com/25590209/184561126-c537a462-bbee-4711-a541-3317a52e62aa.png)
