# auto-input-width
[View Live Demo](http://auto-input-width.bdroutines.com) or [View Live Demo](https://tasmir.github.io/auto-input-width/index.html)

### HTML
```
<label class="input-sizer">
	<span>Name: </span>
	<input type="text" oninput="this.parentNode.dataset.value = this.value" size="4" placeholder="John">
</label>
<label class="input-sizer">
	<span>DOB: </span>
	<input type="text" oninput="this.parentNode.dataset.value = this.value" size="1" placeholder="5">
</label>
<label class="input-sizer stacked">
	<span>Text: </span>
	<textarea oninput="this.parentNode.dataset.value = this.value" rows="1" placeholder="hi"></textarea>
</label>
```

### SCRIPT
```
<script>
	window.console = window.console || function(t) {};
	if (document.location.search.match(/type=embed/gi)) {
		window.parent.postMessage("resize", "*");
	}
</script>
```

### STYLE
```
<style>
	*, *::before, *::after {
		box-sizing: border-box;
	}

	.input-sizer {
		display: inline-grid;
		vertical-align: top;
		align-items: center;
		position: relative;
		border: solid 1px;
		padding: 0.25em 0.5em;
		margin: 5px;
	}
	.input-sizer.stacked {
		padding: 0.5em;
		align-items: stretch;
	}
	.input-sizer.stacked::after,
	.input-sizer.stacked input,
	.input-sizer.stacked textarea {
		grid-area: 2/1;
	}
	.input-sizer::after,
	.input-sizer input,
	.input-sizer textarea {
		width: auto;
		min-width: 1em;
		grid-area: 1/2;
		font: inherit;
		padding: 0.25em;
		margin: 0;
		resize: none;
		background: none;
		-webkit-appearance: none;
		-moz-appearance: none;
		appearance: none;
		border: none;
	}
	.input-sizer span {
		padding: 0.25em;
	}
	.input-sizer::after {
		content: attr(data-value) " ";
		visibility: hidden;
		white-space: pre-wrap;
	}
	.input-sizer:focus-within {
		outline: solid 1px blue;
	}
	.input-sizer:focus-within > span {
		color: blue;
	}
	.input-sizer:focus-within textarea:focus,
	.input-sizer:focus-within input:focus {
		outline: none;
	}
	.input-sizer > span {
		text-transform: uppercase;
		font-size: 0.8em;
		font-weight: bold;
	}
</style>
```

### DEPENDENCY
```
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/normalize/5.0.0/normalize.min.css">
```

## Complete Model
```
<html lang="en">
<head>

	<meta charset="UTF-8">

	<meta name="viewport" content="width=device-width, initial-scale=1">

	<title>Auto Input Width</title>

	DEPENDENCY PART 

	STYLE PART 

	SCRIPT PART

</head>

<body translate="no" data-new-gr-c-s-check-loaded="14.1008.0" data-gr-ext-installed="">
	HTML PART
</body>
</html>
```
