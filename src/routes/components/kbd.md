---
layout: componentLayout
title: Svelte KBD (Keyboard) - Flowbite
breadcrumb_title: KBD
dir: Components
description: Use the KBD component as an inline element to denote textual user input from the keyboard inside paragraphs, tables, and other components
---

<MetaTag {breadcrumb_title} {title} {dir} {description}/>

<script>
  import { Htwo, PageHeadSection, TableProp, TableDefaultRow, MetaTag } from '../utils'
  import { Breadcrumb, BreadcrumbItem, Heading, P, A } from '$lib'
  import { props as items} from '../props/Kbd.json'
  import { props as items2} from '../props/ArrowKeyDown.json'
  import { props as items3} from '../props/ArrowKeyLeft.json'
  import { props as items4} from '../props/ArrowKeyRight.json'
  import { props as items5} from '../props/ArrowKeyUp.json'

  let propHeader = ['Name', 'Type', 'Default']
  let divClass='w-full relative overflow-x-auto shadow-md sm:rounded-lg py-4'
  let theadClass ='text-xs text-gray-700 uppercase bg-gray-50 dark:bg-gray-700 dark:text-white'
  // lib files
  const libFiles = import.meta.glob('../../lib/kbd/*.svelte')
</script>

<PageHeadSection {dir} {breadcrumb_title} {title} {description} {libFiles}/>

The KBD (Keyboard) component can be used to indicate a textual user input from the keyboard inside other elements such as in text, tables, cards, and more.

<Htwo label="Setup" />

```html
<script>
  import { Kbd } from 'flowbite-svelte'
</script>
```

<Htwo label="Default KBD" />

Here’s a list of KBD components that you can use inside any other element.

```svelte example hideScript
<script>
  import { Kbd } from 'flowbite-svelte'
</script>

<Kbd class='px-2 py-1.5'>Shift</Kbd>
<Kbd class='px-2 py-1.5'>Ctrl</Kbd>
<Kbd class='px-2 py-1.5'>Tab</Kbd>
<Kbd class='px-2 py-1.5'>Caps Lock</Kbd>
<Kbd class='px-2 py-1.5'>Esc</Kbd>
<Kbd class='px-4 py-1.5'>Spacebar</Kbd>
<Kbd class='px-2 py-1.5'>Enter</Kbd>
```

<Htwo label="KBD inside text" />

Use this example by nesting an inline KBD component inside a paragraph.

```svelte example hideScript
<script>
  import { Kbd } from 'flowbite-svelte'
</script>

<p class="text-gray-500 dark:text-gray-400">
Please press <Kbd class="px-2 py-1.5">Ctrl</Kbd> + <Kbd class="px-2 py-1.5">Shift</Kbd> + <Kbd class="px-2 py-1.5">R</Kbd> to re-render an MDN page.
</p>
```

<Htwo label="KBD inside table" />

The KBD component can also be used inside table components to denote what type of key can be pressed for certain descriptions.

```svelte example
<script>
  import { Kbd, Table, TableHead, TableHeadCell, TableBody, TableBodyCell, TableBodyRow, ArrowKeyUp, ArrowKeyDown, ArrowKeyRight, ArrowKeyLeft } from 'flowbite-svelte'
</script>

<Table>
  <TableHead>
    <TableHeadCell>Key</TableHeadCell>
    <TableHeadCell>Description</TableHeadCell>
  </TableHead>
  <TableBody class="divide-y">
    <TableBodyRow>
      <TableBodyCell>
        <Kbd class='px-2 py-1.5'>Shift</Kbd> or <Kbd class='px-2 py-1.5'>Tab</Kbd>
      </TableBodyCell>
      <TableBodyCell>Navigate to interactive elements</TableBodyCell>
    </TableBodyRow>
    <TableBodyRow>
      <TableBodyCell>
        <Kbd class='px-2 py-1.5'>Enter</Kbd> or <Kbd class='px-4 py-1.5'>Space bar</Kbd>
      </TableBodyCell>
      <TableBodyCell>Ensure elements with ARIA role="button" can be activated with both key commands.</TableBodyCell>
    </TableBodyRow>
    <TableBodyRow>
      <TableBodyCell>
        <Kbd class="inline-flex items-center mr-1 px-2 py-1.5" >
        <ArrowKeyUp />
        <span class="sr-only">Arrow key up</span>
        </Kbd>
        <Kbd class="inline-flex items-center mr-1 px-2 py-1.5" >
        <ArrowKeyDown />
        <span class="sr-only">Arrow key down</span>
        </Kbd> or 
        <Kbd class="inline-flex items-center mr-1 px-2 py-1.5" >
        <ArrowKeyLeft />
        <span class="sr-only">Arrow key left</span>
        </Kbd>
        <Kbd class="inline-flex items-center mr-1 px-2 py-1.5" >
        <ArrowKeyRight />
        <span class="sr-only">Arrow key right</span>
        </Kbd>
      </TableBodyCell>
      <TableBodyCell>Choose and activate previous/next tab.</TableBodyCell>
    </TableBodyRow>
  </TableBody>
</Table>
```

<Htwo label='Arrow keys' />

Use this example to show arrow keys inside the KBD styled element.

```svelte example
<script>
  import { Kbd, ArrowKeyUp, ArrowKeyDown, ArrowKeyRight, ArrowKeyLeft } from 'flowbite-svelte'
</script>

<Kbd class="inline-flex items-center mr-1 px-2 py-1.5" >
  <ArrowKeyUp />
  <span class="sr-only">Arrow key up</span>
</Kbd>
<Kbd class="inline-flex items-center mr-1 px-2 py-1.5" >
  <ArrowKeyDown />
  <span class="sr-only">Arrow key down</span>
</Kbd>
<Kbd class="inline-flex items-center mr-1 px-2 py-1.5" >
  <ArrowKeyLeft />
  <span class="sr-only">Arrow key left</span>
</Kbd>
<Kbd class="inline-flex items-center mr-1 px-2 py-1.5" >
  <ArrowKeyRight />
  <span class="sr-only">Arrow key right</span>
</Kbd>
```

<Htwo label='Letter keys' />

Use this example if you need to show a key from the latin alphabet

```svelte example hideScript
<script>
  import { Kbd } from 'flowbite-svelte'
</script>

<Kbd class="px-2 py-1.5">Q</Kbd>
<Kbd class="px-2 py-1.5">W</Kbd>
<Kbd class="px-2 py-1.5">E</Kbd>
<Kbd class="px-2 py-1.5">R</Kbd>
<Kbd class="px-2 py-1.5">T</Kbd>
<Kbd class="px-2 py-1.5">Y</Kbd>
<Kbd class="px-2 py-1.5">U</Kbd>
<Kbd class="px-2 py-1.5">I</Kbd>
<Kbd class="px-2 py-1.5">O</Kbd>
<Kbd class="px-2 py-1.5">P</Kbd>
<Kbd class="px-2 py-1.5">A</Kbd>
<Kbd class="px-2 py-1.5">S</Kbd>
<Kbd class="px-2 py-1.5">D</Kbd>
<Kbd class="px-2 py-1.5">F</Kbd>
<Kbd class="px-2 py-1.5">G</Kbd>
<Kbd class="px-2 py-1.5">H</Kbd>
<Kbd class="px-2 py-1.5">J</Kbd>
<Kbd class="px-2 py-1.5">K</Kbd>
<Kbd class="px-2 py-1.5">L</Kbd>
<Kbd class="px-2 py-1.5">Z</Kbd>
<Kbd class="px-2 py-1.5">X</Kbd>
<Kbd class="px-2 py-1.5">C</Kbd>
<Kbd class="px-2 py-1.5">V</Kbd>
<Kbd class="px-2 py-1.5">B</Kbd>
<Kbd class="px-2 py-1.5">N</Kbd>
<Kbd class="px-2 py-1.5">M</Kbd>
```

<Htwo label='Number keys' />

Use this example to show a key inside a KBD component from the english numeral system.

```svelte example hideScript
<script>
  import { Kbd } from 'flowbite-svelte'
</script>

<Kbd class="px-2 py-1.5">1</Kbd>
<Kbd class="px-2 py-1.5">2</Kbd>
<Kbd class="px-2 py-1.5">3</Kbd>
<Kbd class="px-2 py-1.5">4</Kbd>
<Kbd class="px-2 py-1.5">5</Kbd>
<Kbd class="px-2 py-1.5">6</Kbd>
<Kbd class="px-2 py-1.5">7</Kbd>
<Kbd class="px-2 py-1.5">8</Kbd>
<Kbd class="px-2 py-1.5">9</Kbd>
<Kbd class="px-2 py-1.5">0</Kbd>
```

<Htwo label='Function keys' />

This example can be used to denote function keys inside the KBD component.

```svelte example hideScript
<script>
  import { Kbd } from 'flowbite-svelte'
</script>

<Kbd class="px-2 py-1.5">F1</Kbd>
<Kbd class="px-2 py-1.5">F2</Kbd>
<Kbd class="px-2 py-1.5">F3</Kbd>
<Kbd class="px-2 py-1.5">F4</Kbd>
<Kbd class="px-2 py-1.5">F5</Kbd>
<Kbd class="px-2 py-1.5">F6</Kbd>
<Kbd class="px-2 py-1.5">F7</Kbd>
<Kbd class="px-2 py-1.5">F8</Kbd>
<Kbd class="px-2 py-1.5">F9</Kbd>
<Kbd class="px-2 py-1.5">F10</Kbd>
<Kbd class="px-2 py-1.5">F11</Kbd>
<Kbd class="px-2 py-1.5">F12</Kbd>
```

<Htwo label="Props" />

<p>The component has the following props, type, and default values. See <A href="/pages/types">types 
 page</A> for type information.</p>

<h3 class='text-xl w-full dark:text-white py-4'>Kbd</h3>

<TableProp header={propHeader} {divClass} {theadClass}>
  <TableDefaultRow items={items} rowState='hover' />
</TableProp>

<h3 class='text-xl w-full dark:text-white py-4'>ArrowKeyDown</h3>

<TableProp header={propHeader} {divClass} {theadClass}>
  <TableDefaultRow items={items2} rowState='hover' />
</TableProp>

<h3 class='text-xl w-full dark:text-white py-4'>ArrowKeyLeft</h3>

<TableProp header={propHeader} {divClass} {theadClass}>
  <TableDefaultRow items={items3} rowState='hover' />
</TableProp>

<h3 class='text-xl w-full dark:text-white py-4'>ArrowKeyRight</h3>

<TableProp header={propHeader} {divClass} {theadClass}>
  <TableDefaultRow items={items4} rowState='hover' />
</TableProp>

<h3 class='text-xl w-full dark:text-white py-4'>ArrowKeyUp</h3>

<TableProp header={propHeader} {divClass} {theadClass}>
  <TableDefaultRow items={items5} rowState='hover' />
</TableProp>

<Htwo label="References" />

<P>
  <A href="https://flowbite.com/docs/components/kbd/" target="_blank" rel="noreferrer" class="link"
    >Tailwind CSS KBD (Keyboard)</A
  >
</P>
