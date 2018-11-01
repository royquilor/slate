---
title: API Reference

language_tabs: # must be one of https://git.io/vQNgJ
  - javascript

toc_footers:
  - <a href='#'>Sign Up for a Developer Key</a>
  - <a href='https://github.com/lord/slate'>Documentation Powered by Slate</a>

includes:

  - setup/README
  - setup/1-project-setup
  - setup/2-elasticsearch
  - setup/3-indexing
  - setup/4-using-components
  - setup/5-default-query
  - setup/6-extending-components

  - components/README
  - components/basics/search-box
  - components/basics/hits
  - components/basics/nohits
  - components/basics/initial-loader

  - components/navigation/pagination
  - components/navigation/refinement-list
  - components/navigation/numeric-refinement-list
  - components/navigation/menu
  - components/navigation/range-filter
  - components/navigation/dynamic-range-filter
  - components/navigation/input-filter
  - components/navigation/checkbox-filter
  - components/navigation/tag-filter
  - components/navigation/selected-filters
  - components/navigation/grouped-selected-filters
  - components/navigation/reset
  - components/navigation/hierarchical-menu
  - components/navigation/hierarchical-refinement-filter

  - components/display/switcher
  - components/display/page-size-selector

  - components/sorting/sort

  - components/metadata/stats

  - components/ui/layout-components
  - components/ui/panel
  - components/ui/list-components
  - components/ui/range-components

  - theming/README.md
  - theming/using-searchkit-theme
  - theming/extending-searchkit-theme
  - theming/building-your-own

  - core/README
  - core/Architecture
  - core/SearchkitManager
  - core/Accessors
  - core/ImmutableQuery
  - core/FieldOptions
  - core/QueryDSL
  - core/SearchkitProvider
  - core/SearchkitComponent
  - core/Translate

  - upgrading/README
  - upgrading/migrating_from_0_2
  - upgrading/migrating_from_0_3
  - upgrading/migrating_from_0.4
  - upgrading/migrating_from_0.5
  - upgrading/migrating_from_0.6
  - upgrading/migrating_from_0.7
  - upgrading/migrating_from_0.8
  - upgrading/migrating_from_0.9

  - server/README
  - server/searchkit_express
  - server/indexing

  - developer-guide




search: true
---

# What is Searchkit?

```jsx
const searchkit = new SearchkitManager("http://demo.searchkit.co/api/movies/")

const App = ()=> (
  <SearchkitProvider searchkit={searchkit}>
    <Layout>
      <TopBar>
        <SearchBox
          autofocus={true}
          searchOnChange={true}
          prefixQueryFields={["actors^1","type^2","languages","title^10"]}/>
      </TopBar>
      <LayoutBody>
        <SideBar>
          <HierarchicalMenuFilter
            fields={["type.raw", "genres.raw"]}
            title="Categories"
            id="categories"/>
          <RefinementListFilter
            id="actors"
            title="Actors"
            field="actors.raw"
            operator="AND"
            size={10}/>
        </SideBar>
        <LayoutResults>
          <ActionBar>

            <ActionBarRow>
              <HitsStats/>
            </ActionBarRow>

            <ActionBarRow>
              <SelectedFilters/>
              <ResetFilters/>
            </ActionBarRow>

          </ActionBar>
          <Hits mod="sk-hits-grid" hitsPerPage={10} itemComponent={MovieHitsGridItem}
            sourceFilter={["title", "poster", "imdbId"]}/>
          <NoHits/>
        </LayoutResults>
      </LayoutBody>
    </Layout>
  </SearchkitProvider>
)

ReactDOM.render(<App/>, document.getElementById('root'))

```
Searchkit is a suite of UI components built in react. The aim is rapidly create beautiful search applications using declarative components, and without being an ElasticSearch expert.

<img src="./images/codepreview.png"/>

See [Getting Started](/setup/README.md)
[Live demo](http://demo.searchkit.co)
