# Magnific Popup Photo Gallery
Whether you're showcasing your work or team - displaying images on the web is commonplace but how you display them is another matter altogether. Using [Magnific Popup by Dmtry Semenov](http://dimsemenov.com/plugins/magnific-popup/), [Solodev](https://www.solodev.com/) has incorporate impressive photo galleries in a number of projects.

## Tutorial

For detailed instructions, view Solodev's [Enhance your Photo Gallery with Magnific Popup](https://www.solodev.com/blog/web-design/code-examples/enhance-your-photo-gallery-with-magnific-popup.stml) article.

## Demo

Check out a working example on [JSFiddle](https://jsfiddle.net/solodev/pcd8qtL8/).

## HTML

The gallery includes the following HTML markup:
```
<div class="container">
  <div class="popup-gallery">

    <div class="row">
      <div class="col-md-4">
        <div class="resources-item">
          <div class="resources-category-image">
            <a href="images/environment.jpg" title="The Image"><img alt="" src="images/environment.jpg"></a>
          </div>
          <div class="resources-description">
            <p>Published: June 24, 2016</p>
            <h4>Environment</h4>
          </div>
        </div>
      </div>

      <div class="col-md-4">
        <div class="resources-item">
          <div class="resources-category-image">
            <a href="images/architecture.jpg" title="The Image"><img alt="" src="images/architecture.jpg"></a>
          </div>
          <div class="resources-description">
            <p>Published: July 5, 2016</p>
            <h4>Architecture</h4>
          </div>
        </div>
      </div>

      <div class="col-md-4">
        <div class="resources-item">
          <div class="resources-category-image">
            <a href="images/design.jpg" title="The Image"><img alt="" src="images/design.jpg"></a>
          </div>
          <div class="resources-description">
            <p>Published: August 1, 2016</p>
            <h4>Design</h4>
          </div>
        </div>
      </div>
    </div>
    
  </div>
</div>
```

## CSS

All necessary CSS is in magnific-popup.css.

## JavaScript

JavaScript to initialize the pop up is in magnific-popup.js.
```
$(document).ready(function() {
	$('.popup-gallery').magnificPopup({
		delegate: 'a',
		type: 'image',
		tLoading: 'Loading image #%curr%...',
		mainClass: 'mfp-img-mobile',
		gallery: {
			enabled: true,
			navigateByImgClick: true,
			preload: [0,1] // Will preload 0 - before current, and 1 after the current image
		},
		image: {
			tError: '<a href="%url%">The image #%curr%</a> could not be loaded.',
			titleSrc: function(item) {
				return item.el.attr('title') + '<small>by WebCorpCo</small>';
			}
		}
	});
});
```

## External Includes

The contact page includes the following third-party resources:
```
<link rel="stylesheet" type="text/css" href="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.6/css/bootstrap.min.css">    
<link rel="stylesheet" type="text/css" href="https://cdn.jsdelivr.net/jquery.magnific-popup/1.0.0/magnific-popup.css">  
<script type="text/javascript" src="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.6/js/bootstrap.min.js"></script>  
<script type="text/javascript" src="https://ajax.googleapis.com/ajax/libs/jquery/1.12.4/jquery.min.js"></script>   		
<script type="text/javascript" src="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.6/js/bootstrap.min.js"></script>
<script type="text/javascript" src="https://cdn.jsdelivr.net/jquery.magnific-popup/1.0.0/jquery.magnific-popup.js"></script>  
```
