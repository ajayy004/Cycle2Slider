Cycle2Slider
============
# Progressive Loading

Basic Structure need to be followed while creating a progressive loader

```sh
  <div class="cycle-slideshow" 
    data-cycle-timeout=2000
    data-cycle-loader=true
    data-cycle-progressive="#images" // You need to mention the id/class to have the progressive loading, Basicly it tell to not start loading till the dom is not loaded completly
    >
    <!-- markup  delecared over here will be loaded as the dom loads-->
    <img src="assets/images/slider-1.jpg">

    <!-- When the DOM is totally loaded the below code will start loading-->
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
