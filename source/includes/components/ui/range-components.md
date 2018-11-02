## Range Components
A Suite of UI Components which render ranges in various ways and can be passed to some Searchkit components to change their range appearance.

![Example](ui/range-components.png)

Currently works for `RangeFilter` using the `rangeComponent` prop

### RangeSliderHistogram

RangeFilter's default style

![Example](ui/range-slider-histogram.png)

### RangeSliderHistogramInput

Full-featured range component with a slider, histogram, and input. All other current range components are slimmed-down versions of this one.

![Example](ui/range-slider-histogram-input.png)

### RangeInput

Range component containing only min/max input fields. Requires pressing "Go" to update the filter.

![Example](ui/range-input.png)

### RangeSlider

Simple slider, using `rc-slider`. Updates the filter when the handle is released.

![Example](ui/range-slider.png)

### RangeHistogram

Renders a histogram with no filtering possibilities.

![Example](ui/range-histogram.png)

### RangeSliderInput

![Example](ui/range-slider-input.png)

### RangeHistogramInput

![Example](ui/range-histogram-input.png)

### Compatible parent components

#### RangeFilter

Works with all range components
