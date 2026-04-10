# CSS3 Assessment Solutions

## Question 13

### Question

![Question 13](../assets/question13.png)

### Answer

The paragraph will initially have a white text color and a grey background. After a delay of 3 seconds, the animation `myfirst` will start and run for 8 seconds in reverse direction. The animation will transition the paragraph's text color and background color from `yellow` and `pink` (100% keyframe) to `aqua` and `black` (0% keyframe) due to the `animation-direction: reverse;` property. The `animation-fill-mode: backwards;` ensures that the paragraph takes the styles defined at the 0% keyframe before the animation starts.