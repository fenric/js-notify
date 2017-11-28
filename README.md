# Simple Timer

### Install via bower
```
bower install fenric-js-notify
```

### Using after install via bower
```
<link type="text/css" href="bower_components/fenric-js-notify/src/notify.css" rel="stylesheet" />
<script type="text/javascript" src="bower_components/fenric-js-notify/src/notify.js"></script>
```

### Example
```
new $notify(function(notify)
{
	// notify.TYPE_INFO
	// notify.TYPE_SUCCESS
	// notify.TYPE_WARNING
	// notify.TYPE_ERROR
	notify.setType(notify.TYPE_INFO);

	// notify.POSITION_TOP_RIGHT
	// notify.POSITION_RIGHT_BOTTOM
	// notify.POSITION_BOTTOM_LEFT
	// notify.POSITION_LEFT_TOP
	notify.setPosition(notify.POSITION_TOP_RIGHT);

	// 1000 - one second
	// <= 0 - infinitely
	notify.setLifetime(-1);

	// Set a icon of the Notify
	notify.setIcon('fa fa-info');

	// Set a title of the Notify
	notify.setTitle('...');

	// HTML message
	notify.setMessage('...', true);

	// Text message
	notify.setMessage('...', false);

	// Display the Notify
	notify.display();

	// Close (destroy) the Notify
	notify.close();

	// Events:
	notify.onDisplay(function() {
		// some code, with using this...
	});
	notify.onClick(function(event) {
		// some code, with using this...
	});
	notify.onHover(function(event) {
		// some code, with using this...
	});
	notify.onClose(function() {
		// some code, with using this...
	});
});
```
