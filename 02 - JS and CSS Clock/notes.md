Review - http://thesagittariusme.blogspot.com/2017/01/js30-day2-clock.html

```
transform-origin:100%; //moves the origin of rotation along x-axis

```

Then, I learned about transition-timing-function
The normal values are ease-in, ease-out, ease-in-out
But we can customize the transition using a cubic bezier curve, like so, to give __ticking sensation__:
```
transition-timing-function: cubic-bezier(0.1,2,7,0.58,1);
```


The setInterval function runs a function passed to it on every interval specified
```
setInterval(functionName, milliseconds)
```
We have used it to call setDate function after every second. 
setDate is the function in which all the hours, minutes and seconds are retrieved and degrees for the hands are calculated and applied

To bypass this, just change the transition to ‘all 0s’ using javascript.
I created a class called .fast
It contains the following line of code
```
transition: all 0s;
```

At every 0, I add the class and at every 1, I remove the class thus returning the hand to the cubic bezier curve at 0.05s
```
if(seconds===0)
secondHand.classList.add(‘fast’);
if(seconds===1)
secondHand.classList.remove(‘fast’);
```