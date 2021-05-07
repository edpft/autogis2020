# Exercise 1

## Problem 1.1

### Python

```{python}
from typing import Tuple

from shapely.geometry import Point

def create_point_geom(x_coord: float, y_coord: float) -> Point:
    return Point((x_coord, y_coord))
```

### Julia

```{julia}
using GeoInterface

function create_point_geom(x_coord::Number, y_coord::Number)::Point
    return Point(x_coord, y_coord)
end
```

### Rust

```{rust}
use geo_types::Point;

fn create_point_geom(x_coord: f64, y_coord: f64) -> Point<f64> {
    Point::new(x_coord, y_coord)
}
```

## Problem 1.2

### Python

```{python}
from typing import List

from shapely.geometry import LineString, Point

def create_line_geom(points: List[Point]) -> LineString:
    assert type(points) == list, "Input should be a list!"
    assert len(points) >= 2, "LineString object requires at least two Points!"
    line = LineString(points)
    return line
```

## Problem 1.3