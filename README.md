# css-shapes

A scss library for working with clips and shapes

## Usage

css-shapes is based on css clip-path and related specs and provides you with an extendable set of the most basic shapes.

The following shapes are currently included with the default configuration:
`circle`, `triangle`, `triangle-orthogonal`, `trapezoid`, `parallelogram`, `rhombus`, `pentagon`, `hexagon`, `heptagon`, `octagon`, `nonagon`, `decagon`, `bevel`, `rabbet`, `arrow-left`, `arrow-right`, `point-left`, `point-right`, `chevron-left`, `chevron-right`, `star`

All shapes are accessible as css-properties prefixed with `--shape-`, e.g. `--shape-circle`. More shapes can be added via `scss`

Furthermore, all shapes are rotated by `90deg`, `180deg`, `270deg`. These can be accessed by adding suffix `-rotate-90`, e.g. `--shape-triangle-rotate-90`. Rotation steps can be configured via `scss`.


### CSS Classes
For every shape, the following css-classes are autogenerated containing vendor-prefixed assignments.

#### .clip-{shape}


Adds `clip-path` of the specified shape

```html
<img class=".clip-circle"/>
```

#### .shape-outside-{shape}

Adds `shape-outside` of the specified shape

```html
<img class=".shape-outside-circle"/>
```


### SCSS

Adjust shapes and rotation-steps by scss variables:

```scss
// Custom shapes
$shapes: map-merge((
  custom-shape: polygon(50% 0%, 90% 20%, 100% 60%, 75% 100%, 25% 100%, 0% 60%, 10% 20%)
), $shapes);

// Rotate
$shape-rotate-steps: (90deg, 180deg, 270deg);
$shape-rotate-origin: (50%, 50%);
```



## Development

Download and install [NodeJS](https://nodejs.org).

Point the terminal at your project directory and install dependencies

```cli
npm i
```

Run dev server

```cli
npm start
```

## Production

Trigger a production build

```cli
npm run build
```

### Deployment

The demo is deployed to its github-page by issuing the following command:

```cli
npm run deploy
```
