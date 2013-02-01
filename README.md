# Featured Image Zoomer #

*Description:* This script lets you view a magnified portion of any image upon moving your mouse over it. A magnifying area appears alongside the image displaying the magnified image on demand. The user can toggle the zoom level by using the mousewheel.  It's great to use on product images, photos, or other images with lots of details you want users to be able to get into on command.

## Directions ##

*Step 1:* This script uses the following external files:

+ jQuery 1.7 or above (served via Google CDN)
+ multizoom.js
+ multizoom.css

*Step 2:* Add the below code to the HEAD section of your page:

	<link rel="stylesheet" href="multizoom.css" type="text/css" />
	
	<script type="text/javascript" src="http://ajax.googleapis.com/ajax/libs/jquery/1.8/jquery.min.js"></script>
	
	<script type="text/javascript" src="multizoom.js">
	
	// Featured Image Zoomer (w/ optional multizoom and adjustable power)- By Dynamic Drive DHTML code library (www.dynamicdrive.com)
	// Multi-Zoom code (c)2012 John Davenport Scheuer
	// as first seen in http://www.dynamicdrive.com/forums/
	// username: jscheuer1 - This Notice Must Remain for Legal Use
	// Visit Dynamic Drive at http://www.dynamicdrive.com/ for this script and 100s more
	
	</script>
	
	<script type="text/javascript">
	
	jQuery(document).ready(function($){
	
		$('#image1').addimagezoom({ // single image zoom
			zoomrange: [3, 10],
			magnifiersize: [300,300],
			magnifierpos: 'right',
			cursorshade: true,
			largeimage: 'hayden.jpg' //<-- No comma after last option!
		})
	
	
		$('#image2').addimagezoom() // single image zoom with default options
		
		$('#multizoom1').addimagezoom({ // multi-zoom: options same as for previous Featured Image Zoomer's addimagezoom unless noted as '- new'
			descArea: '#description', // description selector (optional - but required if descriptions are used) - new
			speed: 1500, // duration of fade in for new zoomable images (in milliseconds, optional) - new
			descpos: true, // if set to true - description position follows image position at a set distance, defaults to false (optional) - new
			imagevertcenter: true, // zoomable image centers vertically in its container (optional) - new
			magvertcenter: true, // magnified area centers vertically in relation to the zoomable image (optional) - new
			zoomrange: [3, 10],
			magnifiersize: [250,250],
			magnifierpos: 'right',
			cursorshadecolor: '#fdffd5',
			cursorshade: true //<-- No comma after last option!
		});
		
		$('#multizoom2').addimagezoom({ // multi-zoom: options same as for previous Featured Image Zoomer's addimagezoom unless noted as '- new'
			descArea: '#description2', // description selector (optional - but required if descriptions are used) - new
			disablewheel: true // even without variable zoom, mousewheel will not shift image position while mouse is over image (optional) - new
					//^-- No comma after last option!	
		});
		
	})
	
	</script>


*Step 3:* Then, add the below sample markup to your page:

	<h3>Demo 1:</h3>
	
	<img id="image1" border="0" src="haydensmall.jpg" style="width:250px;height:338px">
	
	
	
	
	<h3>Demo 2:</h3>
	
	<img id="image2" border="0" src="listenmusic.jpg" style="width:200px;height:150px">
	
	
	
	
	<h3>Demo 3:</h3>
	
	<div class="targetarea" style="border:1px solid #eee"><img id="multizoom1" alt="zoomable" title="" src="millasmall.jpg"/></div>
	<div id="description">Milla Jojovitch</div>
	<div class="multizoom1 thumbs">
	<a href="millasmall.jpg" data-large="milla.jpg" data-title="Milla Jojovitch"><img src="milla_tmb.jpg" alt="Milla" title=""/></a> 
	<a href="saleensmall.jpg" data-lens="false" data-magsize="150,150" data-large="saleen.jpg" data-title="Saleen S7 Twin Turbo"><img src="saleen_tmb.jpg" alt="Saleen" title=""/></a> 
	<a href="haydensmall.jpg" data-large="hayden.jpg" data-title="Hayden Panettiere"><img src="hayden_tmb.jpg" alt="Hayden" title=""/></a> 
	<a href="jaguarsmall.jpg" data-large="jaguar.jpg" data-title="Jaguar Type E"><img src="jaguar_tmb.jpg" alt="Jaguar" title=""/></a>
	</div>
	
	
	
	
	<h3>Demo 4:</h3>
	
	<div class="targetarea diffheight"><img id="multizoom2" alt="zoomable" title="" src="angelinasmall.jpg"/></div>
	<div id="description2">Angelina Jolie</div>
	<div class="multizoom2 thumbs">
	<a href="angelinasmall.jpg" data-large="angelina.jpg" data-title="Angelina Jolie"><img src="angelina_tmb.jpg" alt="Angelina" title=""/></a>
	<a href="saleensmall.jpg" data-large="saleen.jpg" data-title="Saleen S7 Twin Turbo"><img src="saleen_tmb.jpg" alt="Saleen" title=""/></a>
	<a href="jaguarsmall.jpg" data-large="jaguar.jpg" data-title="Jaguar Type E"><img src="jaguar_tmb.jpg" alt="Jaguar" title=""/></a>
	<a href="listenmusic.jpg" data-title="Relaxing Music" data-dims="300, 225"><img src="listen_tmb.jpg" alt="Relaxing Music" title=""/></a>
	</div>


## Featured Image Zoomer set up ##

See script project page for additional details on setup and documentation: <http://www.dynamicdrive.com/dynamicindex4/featuredzoomer.htm>
