Cycle2Slider
============
# Progressive Loading

Basic Structure need to be followed while creating a progressive loader
![alt tag](https://raw.github.com/ajaykumaryadav/Cycle2Slider/master/waterfall%20loading%20chart.jpg)


```sh
  <div class="cycle-slideshow" 
    data-cycle-timeout=2000
    data-cycle-loader=true
    data-cycle-progressive="#images" # You need to mention the id/class to have the progressive loading, Basicly it tell to not start loading till the dom is not loaded completly
    >
    #Markup declared below will be loaded as the DOM loaded
    <img src="assets/images/slider-1.jpg">

    #When the DOM is completely loaded the below code then start loading
    <script id="images" type="text/cycle">
		[
		    "<img src='assets/images/slider-2.jpg'>",
		    "<img src='assets/images/slider-3.jpg'>",
		    "<img src='assets/images/slider-4.jpg'>",
		    ...
		    "<img src='assets/images/slider-10.jpg'>"				    
		]
    </script>
   </div>
   
```
```sh
	<div class="cycle-slideshow slider" 
		data-cycle-timeout=2000
		data-cycle-loader=true
		data-cycle-progressive="#slider"
		data-cycle-slides=">div"
	>
		#Markup declared below will be loaded as the DOM loaded
		<div>
			<img src="assets/images/slider-1.jpg">
			<span>Slider image 1</span>
		</div>
		#Using the data-cycle-split you can define the split pattern that tells cycle2 that its the end of one slide
		<script id="slider" type="text/cycle" data-cycle-split="---">
			<div>
				<img src='assets/images/slider-2.jpg'>
				<span>Slider image 2</span>
			</div>
			---
			<div>
				<img src='assets/images/slider-3.jpg'>
				<span>Slider image 3</span>
			</div>
			---
			...
			---
			<div>
				<img src='assets/images/slider-10.jpg'>
				<span>Slider image 10</span>
			</div>
		</script>
	</div>   
```
