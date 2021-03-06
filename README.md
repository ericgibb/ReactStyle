React Style component (PoC)
==========

Make your React components visually predictable. React Style components allows you to cascade CSS stylesheets on your components, automatically namespacing them.

Inspired by the [SUIT CSS](https://suitcss.github.io/) methodology.

### Demo:

[Mao-mao-mao!](https://edealer.nl/mao)

### Example:

You write:

```javascript
		/** @jsx React.DOM */

		var Profile = React.createClass({
			render: function () {
				return (
					<Style sheet="
						.card {
							cursor: pointer;
							margin: 15px;
							padding: 15px;
							text-align: center;
							height: 200px;
						}
						img {
							width: 130px;
							height: 130px;
						}
						p {
							margin: 10px;
						}
						">
						<div className="card">
							<img src="mao.jpg" />
							<p>Mao</p>
						</div>
					</Style>
				);
			}
		});
```

You get namespaced CSS that works on sub-components (comparable to HTML5 `<style scoped>`):

```html
<div class="Style-4n412lnmi">
	<div class="card">
		<img src="mao.jpg">
		<p>Mao</p>
	</div>
	<style>
		.Style-4n412lnmi .card { 
		  cursor: pointer; 
		  margin: 15px; 
		  padding: 15px; 
		  text-align: center; 
		  height: 200px; 
		}
		.Style-4n412lnmi img { 
		  width: 130px; 
		  height: 130px; 
		}
		.Style-4n412lnmi p { 
		  margin: 10px; 
		}
	</style>
</div>
```

For a cascaded effect, see the `index.html` demo.
