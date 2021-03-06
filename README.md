This is a JavaScript library to visualize BPMN 2.0 XML content in the browser. 
The rendering is done with Raphael JS (http://raphaeljs.com/).

All files and their content are licensed under the GNU Affero General Public License v3 (http://www.gnu.org/licenses/agpl-3.0.html),
if not stated otherwise in the individual files.

Quickstart
==========

Include the js files into your html (bpmn.js depends on rapaheljs and dojo at the moment).

This will render the process as SVG representation into an div with id "diagram" :

```javascript

	require(["bpmn/core", "dojo/domReady!"], function(bpmn) {
		    bpmn.parse("test/collaboration.bpmn", function() {
		    	bpmn.highlight(["ServiceTask_1"], {"color" : "red"});
	    	}, 
	    	{
	    		diagramElement: "diagram", 
	    		clickFn : function (elem) {
	    			alert(JSON.stringify(elem));
	    		}
	    	});
	});
```

Todo
====

* Namespace prefix check on element value change
* Flow element containers children
* Boudnary events and labels should always be on top
* Activity / Loop Markers
* Flow labels
* Movable labels
* Movable connection waypoints
* Missing event definitions
