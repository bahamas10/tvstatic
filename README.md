TV Static
=========

Generate TV static in an HTML5 canvas element

View the demo online http://bahamas10.github.com/tvstatic/

Usage
-----

``` html
<script src="tvstatic.js"></script>
<script>
        var canvas, ctx;

		window.addEventListener('load', load, false);
		function load() {
			canvas = document.getElementById('canvas');
			ctx = canvas.getContext('2d');
			ctx.fillStyle = '#000';

			requestAnimationFrame(render);
		}

		function render() {
			requestAnimationFrame(render);
			ctx.clearRect(0, 0, canvas.width, canvas.height);

			tvstatic(canvas, ctx, 2);
		}
</script>
```

tvstatic()
----------

### `tvstatic(canvas, ctx, [scale])

- `canvas`: the canvas object on which to overlay static
- `ctx`: the 2d context of the canvas above
- `scale`: the scale to use when drawing pixels, defaults to 1

License
-------

MIT
