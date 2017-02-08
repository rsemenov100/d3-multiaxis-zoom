d3-xy-zoom
==========

d3 plugin to zoom along X and Y axes independently.

This implementation is a fork from [d3-multiaxis-zoom](https://github.com/mathisonian/d3-multiaxis-zoom).

Given implementation does not use modifier keys or any other key combinations to
trigger zooming/panning along X and/or Y axes. Instead a user should call `setZoomMode`
function and pass one of the `ZoomModeEnum` values.

Thus, the user's app has a full control over toggling of zoom mode. It can be
done by using some key combinations, toggle buttons, toolbar, etc.


![zooming example](./images/zoom.gif)

## Usage

Script Tag:
```html

<script src="http://d3js.org/d3.v3.min.js"></script>
<script src="../path/to/d3-multiaxis-zoom.js"></script>
<script type="text/javascript">

	// Apply to plugin
	d3_multiaxis_zoom(d3);

	// now all d3.behavior.zoom instances will be modified with this plugin

	// Set zooming along X axis only
	d3_multiaxis_zoom.setZoomMode(d3_multiaxis_zoom.ZoomModeEnum.X);

	// Set zooming along Y axis only
	d3_multiaxis_zoom.setZoomMode(d3_multiaxis_zoom.ZoomModeEnum.Y);

	// Set zooming along both axes
	d3_multiaxis_zoom.setZoomMode(d3_multiaxis_zoom.ZoomModeEnum.BOTH);

</script>

```

Browserify:
```js
var d3 = require('d3');
require('d3-multiaxis-zoom')(d3); // apply the plugin

```

## License

MIT
