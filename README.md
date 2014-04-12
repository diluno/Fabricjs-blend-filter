# An image filter for fabric.js that implements several blend modes

Currently supports add, diff, multiply, and screen modes. More to come.

### Usage examples:

Blending image to another image

```javascript
fabric.Image.fromURL('myimage.jpg', function(img) {
  var filter = new fabric.Image.filters.Blend({
    image: image2,
    mode: 'add',
    alpha: 0.5
  });

  img.filters.push(filter);

  // apply filters and re-render canvas when done
  img.applyFilters(canvas.renderAll.bind(canvas));

  // add image onto canvas
  canvas.add(img);
});

```

Blending colors to another image

```javascript
fabric.Image.fromURL('myimage.jpg', function(img) {
  var filter = new fabric.Image.filters.Blend({
    color: '#000',
    mode: 'multiply'
  });

  img.filters.push(filter);

  // apply filters and re-render canvas when done
  img.applyFilters(canvas.renderAll.bind(canvas));

  // add image onto canvas
  canvas.add(img);
});
```

### Note:

Code is still in development stages
