---
layout: tabLayout
---

<script>
  import { FullWidthTabs, Table, TableDefaultRow, Breadcrumb } from '$lib/index'
  import componentProps from '../props/FullWidthTabs.json'
  // Props table
  export let items = componentProps.props
	let propHeader = ['Name', 'Type', 'Default']
	// console.log(items)
	let divClass='w-full relative overflow-x-auto shadow-md sm:rounded-lg'

  let tabLabel = 'Select a target'
  let tabs = [
  {
    name: "Profile",
    active: true,
    href: "/",
    rel: undefined,
  },
  {
    name: "Dashboard",
    active: false,
    href: "/",
  },
  {
    name: "Settings",
    active: false,
    href: "/",
  },
  {
    name: "Contacts",
    active: false,
    href: "/",
  },
];

  let crumbs = [
    {
      label:'Home',
      href:'/'
    },
    {
      label:'Tabs',
      href:'/tabs/'
    },
    {
      label:'Full-width tabs',
      href:'/tabs/full-width-tabs'
    },
  ]
</script>

<Breadcrumb {crumbs}/>

<h1 class="text-3xl w-full dark:text-white py-8">Full Width Tabs</h1>

<h2 class="text-2xl mt-8 dark:text-white py-4">Examples</h2>

<div class="container justify-center rounded-xl mx-auto bg-gradient-to-r bg-white dark:bg-gray-900 border border-gray-200 dark:border-gray-700 p-2 sm:p-6">
<FullWidthTabs {tabs} {tabLabel} />
</div>

```html
<script>
  import { FullWidthTabs } from 'flowbite-svelte'
  let tabLabel = 'Select a target'
  let tabs = [
  {
    name: "Profile",
    active: true,
    href: "/#",
    rel: undefined,
  },
  {
    name: "Dashboard",
    active: false,
    href: "/",
  },
  {
    name: "Settings",
    active: false,
    href: "/",
  },
  {
    name: "Contacts",
    active: false,
    href: "/",
  },
];
</script>

<FullWidthTabs {tabs} {tabLabel}/>
```

<h2 class="text-2xl w-full dark:text-white py-4">Props</h2>

<p>The component has the following props, type, and default values. See <a href="/type-list" class="text-blue-600 hover:underline dark:text-blue-500">type-list page</a> for type information.</p>

<Table header={propHeader} {divClass} >
  <TableDefaultRow {items} rowState='hover' />
</Table>