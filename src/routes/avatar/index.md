---
layout: avatarLayout
---

<script>
  import { Avatar, Table, TableDefaultRow, Breadcrumb } from "$lib/index"
  import alertProp from '../props/Avatar.json'
  // Props table
  export let items = alertProp.props
	let propHeader = ['Name', 'Type', 'Default']
	// console.log(items)
	let divClass='w-full relative overflow-x-auto shadow-md sm:rounded-lg'

  let avatar6 = {
    src: '/images/profile-picture-1.webp',
    alt: 'My avatar',
    size: 6
  }
  let avatar8= {
    src: '/images/profile-picture-1.webp',
    alt: 'My avatar',
    size: 8
  }
  let avatar12 = {
    src: '/images/profile-picture-1.webp',
    alt: 'My avatar',
    size: 12
  }
  let avatar16 = {
    src: '/images/profile-picture-1.webp',
    alt: 'My avatar',
    size: 16
  }
  let avatar24 = {
    src: '/images/profile-picture-1.webp',
    alt: 'My avatar',
    size: 24
  }
  let avatar48 = {
    src: '/images/profile-picture-1.webp',
    alt: 'My avatar',
    size: 48
  }

  let avatar2 = {
    src: '/images/profile-picture-2.webp',
    alt: 'My avatar 2',
    size: 12,
    round: true
  }
  let avatar3 = {
    src: '/images/profile-picture-3.webp',
    alt: 'My avatar 3',
    size: 12,
    border: true,
  }
  let avatar4 = {
    src: '/images/profile-picture-1.webp',
    alt: 'My avatar 4',
    size: 12,
    border: true,
    round: true
  }
  let avatarText ={
    src: '/images/profile-picture-2.webp',
    alt: 'My avatar 4',
    size: 12,
    border: true,
    round: true,
    header:'Jese Leos',
    text:'Joined in August 2014'
  }
  let crumbs = [
    {
      label:'Home',
      href:'/'
    },
    {
      label:'Avatar',
      href:'/avatar/'
    }
  ]
</script>

<Breadcrumb {crumbs}/>

<h1 class="text-3xl w-full dark:text-white py-8">Avatar</h1>

<h2 class="text-2xl w-full dark:text-white py-4">Size</h2>

<p>Select size from  6 | 8 | 12 | 24 | 48.</p>

<div class="rounded-xl w-full my-4 mx-auto bg-gradient-to-r bg-white dark:bg-gray-900 border border-gray-200 dark:border-gray-700 p-2 sm:p-6">
<div class=" flex flex-wrap justify-center space-x-4">
<Avatar avatar={avatar6} />
<Avatar avatar={avatar8}/>
<Avatar avatar={avatar12}/>
<Avatar avatar={avatar24}/>
<Avatar avatar={avatar48}/>
</div>
</div>

```html
<script>
  import { Avatar } from "$lib/index"
  let avatar6 = {
    src: '/images/profile-picture-1.webp',
    alt: 'My avatar',
    size: 6
  }
  let avatar8= {
    src: '/images/profile-picture-1.webp',
    alt: 'My avatar',
    size: 8
  }
  let avatar12 = {
    src: '/images/profile-picture-1.webp',
    alt: 'My avatar',
    size: 12
  }
 
  let avatar24 = {
    src: '/images/profile-picture-1.webp',
    alt: 'My avatar',
    size: 24
  }
  let avatar48 = {
    src: '/images/profile-picture-1.webp',
    alt: 'My avatar',
    size: 48,
  }

</script>

<Avatar avatar={avatar6} />
<Avatar avatar={avatar8}/>
<Avatar avatar={avatar12}/>
<Avatar avatar={avatar24}/>
<Avatar avatar={avatar48}/>

```

<h2 class="text-2xl w-full dark:text-white py-4">Border and round</h2>

<p>Set true to border and/or round.</p>

<div class="rounded-xl w-full my-4 mx-auto bg-gradient-to-r bg-white dark:bg-gray-900 border border-gray-200 dark:border-gray-700 p-2 sm:p-6">
  <div class=" flex flex-wrap justify-center space-x-4">
    <Avatar avatar={avatar2} />
    <Avatar avatar={avatar3} />
    <Avatar avatar={avatar4} />
  </div>
</div>

```html
<script>
  let avatar2 = {
    src: '/images/profile-picture-2.webp',
    alt: 'My avatar 2',
    size: 12,
    round: true
  }
  let avatar3 = {
    src: '/images/profile-picture-3.webp',
    alt: 'My avatar 3',
    size: 12,
    border: true,
  }
  let avatar4 = {
    src: '/images/profile-picture-1.webp',
    alt: 'My avatar 4',
    size: 12,
    border: true,
    round: true
  }
</script>  

<Avatar avatar={avatar2} />
<Avatar avatar={avatar3} />
<Avatar avatar={avatar4} />
```

<h2 class="text-2xl w-full dark:text-white py-4">Placehoder</h2>

<p>By setting placehoder, you display a placeholder avatar.</p>

<div class="rounded-xl w-full my-4 mx-auto bg-gradient-to-r bg-white dark:bg-gray-900 border border-gray-200 dark:border-gray-700 p-2 sm:p-6 flex flex-wrap justify-center">

  <Avatar placehoder />

</div>

```html
<Avatar placehoder />
```

<h2 class="text-2xl w-full dark:text-white py-4">Avatar text</h2>

<p>You can set header and text to show additional information.</p>

<div class="rounded-xl w-full my-4 mx-auto bg-gradient-to-r bg-white dark:bg-gray-900 border border-gray-200 dark:border-gray-700 p-2 sm:p-6 flex flex-wrap justify-center">
  <Avatar avatar={avatarText} />
</div>


```html
<script>
  let avatarText ={
    src: '/images/profile-picture-2.webp',
    alt: 'My avatar 4',
    size: 12,
    border: true,
    round: true,
    header:'Jese Leos',
    text:'Joined in August 2014'
  }
</script>

<Avatar avatar={avatarText} />
```

<h2 class="text-2xl w-full dark:text-white py-4">Props</h2>

<p>The component has the following props, type, and default values. See <a href="/type-list" class="text-blue-600 hover:underline dark:text-blue-500">type-list page</a> for type information.</p>

<Table header={propHeader} {divClass} >
  <TableDefaultRow {items} rowState='hover' />
</Table>