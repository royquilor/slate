## List Components
A Suite of UI Components which render lists in various ways and can be passed to many Searchkit components to change their list appearance.

![Example](navigation/menu-list-components.png)

Many of SearchKit's components which render lists will support a `listComponent` prop where these components an be referenced

### ItemList

Used to render list of facets or items

![Example](navigation/menu-itemlist.png)

### ItemCheckboxList

Used to render list of facets or items when multiselecting

![Example](navigation/menu-checkbox.png)


### ItemHistogramList
Used to render list of facets or items with a histogram bar showing the count. Requires a `doc_count` for each item, so won't work for Pagination, SortingSelector, and other non-filter components.

![Example](navigation/menu-histogram.png)

### TagCloud
Used to render list of facets or items where the count influences the size of text. Requires a `doc_count` for each item, so won't work for Pagination, SortingSelector, and other non-filter components.

![Example](navigation/menu-tagcloud.png)

### Tabs
Used to render tabs, often used for menu or view switching

![Example](navigation/menu-tabs.png)

### Select
Used to render a selectable list of items

![Example](navigation/menu-select.png)

### Toggle
Renders a toggle with single/multiple select behaviour

![Example](navigation/menu-toggle.png)


### Compatible parent components

#### RefinementListFilter
ItemList, ItemCheckboxList, ItemHistogramList, TagCloud, Tabs, Select, Toggle

#### MenuFilter
ItemList, ItemCheckboxList, ItemHistogramList, TagCloud, Tabs, Select, Toggle

#### NumericRefinementListFilter
ItemList, ItemCheckboxList, ItemHistogramList, TagCloud, Tabs, Select, Toggle

#### ViewSwitcherToggle
ItemList, ItemCheckboxList, Tabs, Select, Toggle

#### PageSizeSelector
ItemList, ItemCheckboxList, Tabs, Select, Toggle

#### SortingSelector
ItemList, ItemCheckboxList, Tabs, Select, Toggle

#### Pagination
ItemList, ItemCheckboxList, Tabs, Select, Toggle
