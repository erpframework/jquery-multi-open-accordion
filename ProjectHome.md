If you are looking to have the same look of jQuery UI Accordion and wish that you can keep more than one tap opened, with basic accordion functionality, then this plugin might help you.

If you can improve the performance and plugin option, you are more than welcome :)

## Markup ##
```
<div id="multiOpenAccordion">
	<h3><a href="#">tab 1</a></h3>
	<div>
		Lorem ipsum dolor sit amet
	</div>
	<h3><a href="#">tab 2</a></h3>
	<div>
		Lorem ipsum dolor sit amet
	</div>
	<h3><a href="#">tab 3</a></h3>
	<div>
		Lorem ipsum dolor sit amet
	</div>
	<h3><a href="#">tab 4</a></h3>
	<div>
		Lorem ipsum dolor sit amet
	</div>
</div>
```

## Script ##
```

        // this will make the second tab by default opened (index starts from 0)
        $('#multiOpenAccordion').multiAccordion({active: 1 }); 

        // [ OR ]
        // supports multiple tabs to be opened by default
        $('#multiOpenAccordion').multiAccordion({active: [1, 2, 3] }); 

       // you can also set active:false if you don't want any tab to be opened by default
       $('#multiOpenAccordion').multiAccordion({active: false });
	   
	   // show all tabs
	   $('#multiOpenAccordion').multiAccordion({active: 'all' });
	   
	   // hide all tabs
	   $('#multiOpenAccordion').multiAccordion({active: 'none' });
	   
	   // you can set the options as any jQuery UI plugin using option method
	   $('#multiOpenAccordion').multiAccordion('option', 'active', 'all');
```

## Events ##
```
        /* fired when any tab is clicked, ui here hold clicked tab and its content
	 * ui['tab'] 		// current tab
	 * ui['content'] 	// current tab content (div)
	 */
	click: function(event, ui) {}
	
	// when accordion is initialized, ui here holds a jQuery object to the whole accordion
	init: function(event, ui) {}
	
	// when tab is shown, ui here hold the same as in click event above
	tabShown: function(event, ui) {}
	
	// when tab is hidden, ui here hold the same as in click event above
	tabHidden: function(event, ui) {}
	
	// How can you bind these events ?
	 
	// 1. at plugin initialization
	$('#multiOpenAccordion').multiAccordion({
		active: 'all',
		click: function(event, ui) {
			alert('tab is clicked!');
		}
	});
	
	// 2. after initialization
	$('#multiOpenAccordion').multiOpenAccordion('multiopenaccordionclick', function(){
		alert('also clicked');
	});
```

## Methods ##
```
// destroying the plugin and removing all handlers, and styles
$('#multiOpenAccordion').multiOpenAccordion('destroy');
```

![http://www.filamentgroup.com/examples/RollAUI/images/themeroller_ready_white_200px.png](http://www.filamentgroup.com/examples/RollAUI/images/themeroller_ready_white_200px.png)