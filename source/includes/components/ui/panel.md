## Panel
This is a titled Panel component which can be collapsed, it is the default `containerComponent` used by our filter components

![Example](ui/panel.png)

```jsx
import  {Panel} from "searchkit"

const PanelExample ()=> (
  <Panel title="My Panel" collapsable={true} defaultCollapsed={false}>
    <p>my content...</p>
  </Panel>
)

```


### Props
  - `title` *(string)*  - the title of the panel
  - `collapsable` *(boolean)* - Whether the panel can be collapsed (defaults to false)
  - `defaultCollapsed` *(boolean)* - Whether the panel can be collapsed (defaults to true when collapsable = true)


### Making a filter component collapsable
![Example](ui/panel-menu-collapsable.png)

```jsx
  <MenuFilter field="type.raw" size={10}
    title="Movie Type" id="types"
    containerComponent={<Panel collapsable={true} defaultCollapsed={false}/>}/>
  />
```

### Using an action bar component in a panel
![Example](ui/panel-action-component.png)

```jsx
<Panel title="Selected filters" collapsable={true} defaultCollapsed={false}>
  <GroupedSelectedFilters/>
</Panel>
```
