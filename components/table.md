---
title: "Table"
description: "Learn how to use the Table component in Slate UI."
sidebar_order: 10
---

## Table Component

The `Table` component is a flexible and customizable table element that supports various features like striped rows, hover effects, and responsive design. It is broken down into multiple subcomponents to allow fine-grained control over the table's structure and appearance.

### Props

| Prop        | Type    | Default  | Description                                                                          |
|-------------|---------|----------|--------------------------------------------------------------------------------------|
| `striped`   | Boolean | `false`  | If `true`, adds alternating row colors for better readability.                       |
| `bordered`  | Boolean | `false`  | If `true`, adds borders around the table and cells.                                   |
| `hoverable` | Boolean | `false`  | If `true`, highlights rows when hovered.                                              |
| `responsive`| Boolean | `true`   | If `true`, makes the table scrollable on smaller screens.                             |
| `size`      | String  | `'md'`   | Controls the size of the table. Options: `'sm'`, `'md'`, `'lg'`.                      |

### Usage Examples

#### Basic Table

<x-code-preview>
@verbatim
<x-slate::table size="md">
    <x-slot name="header">
        <x-slate::table-header color="blue">
            <x-slate::table-cell header>ID</x-slate::table-cell>
            <x-slate::table-cell header>Name</x-slate::table-cell>
            <x-slate::table-cell header align="center">Actions</x-slate::table-cell>
        </x-slate::table-header>
    </x-slot>
    <x-slate::table-body>
        @foreach([ ['id' => 1, 'name' => 'Lorem Ipsum', 'email' => 'lorem.ipsum@example.com', 'age' => 29, 'city' => 'New York', 'created_at' => '2024-01-15 08:23:45'], ['id' => 2, 'name' => 'Dolor Ismet', 'email' => 'dolor.ismet@example.com', 'age' => 34, 'city' => 'Los Angeles', 'created_at' => '2024-02-10 14:11:30'], ['id' => 3, 'name' => 'John Doe', 'email' => 'john.doe@example.com', 'age' => 40, 'city' => 'Chicago', 'created_at' => '2024-03-05 09:15:22'], ['id' => 4, 'name' => 'Jane Smith', 'email' => 'jane.smith@example.com', 'age' => 25, 'city' => 'Houston', 'created_at' => '2024-04-12 17:48:03'], ['id' => 5, 'name' => 'Alice Johnson', 'email' => 'alice.johnson@example.com', 'age' => 31, 'city' => 'Phoenix', 'created_at' => '2024-05-22 11:20:15'], ['id' => 6, 'name' => 'Bob Brown', 'email' => 'bob.brown@example.com', 'age' => 27, 'city' => 'Philadelphia', 'created_at' => '2024-06-30 13:35:49'], ['id' => 7, 'name' => 'Charlie Davis', 'email' => 'charlie.davis@example.com', 'age' => 36, 'city' => 'San Antonio', 'created_at' => '2024-07-15 16:10:05'], ['id' => 8, 'name' => 'Eve Wilson', 'email' => 'eve.wilson@example.com', 'age' => 28, 'city' => 'San Diego', 'created_at' => '2024-08-03 10:25:58'], ['id' => 9, 'name' => 'Frank Martin', 'email' => 'frank.martin@example.com', 'age' => 39, 'city' => 'Dallas', 'created_at' => '2024-09-08 19:42:31'], ['id' => 10, 'name' => 'Grace Lee', 'email' => 'grace.lee@example.com', 'age' => 22, 'city' => 'San Jose', 'created_at' => '2024-10-18 08:50:44'], ] as $item)
            <x-slate::table-row>
                <x-slate::table-cell>{{ $item['id'] }}</x-slate::table-cell>
                <x-slate::table-cell>{{ $item['name'] }}</x-slate::table-cell>
                <x-slate::table-cell align="center">
                    <x-slate::button>Edit</x-slate::button>
                    <x-slate::button>Delete</x-slate::button>
                </x-slate::table-cell>
            </x-slate::table-row>
        @endforeach
    </x-slate::table-body>
</x-slate::table>
@endverbatim
</x-code-preview>

#### Striped and Hoverable Table

<x-code-preview>
@verbatim
<x-slate::table striped hoverable size="md" bordered>
    <x-slot name="header">
        <x-slate::table-header color="gray">
            <x-slate::table-cell header>ID</x-slate::table-cell>
            <x-slate::table-cell header>Name</x-slate::table-cell>
            <x-slate::table-cell header align="center">Actions</x-slate::table-cell>
        </x-slate::table-header>
    </x-slot>
    <x-slate::table-body>
        @foreach([ ['id' => 1, 'name' => 'Lorem Ipsum', 'email' => 'lorem.ipsum@example.com', 'age' => 29, 'city' => 'New York', 'created_at' => '2024-01-15 08:23:45'], ['id' => 2, 'name' => 'Dolor Ismet', 'email' => 'dolor.ismet@example.com', 'age' => 34, 'city' => 'Los Angeles', 'created_at' => '2024-02-10 14:11:30'], ['id' => 3, 'name' => 'John Doe', 'email' => 'john.doe@example.com', 'age' => 40, 'city' => 'Chicago', 'created_at' => '2024-03-05 09:15:22'], ['id' => 4, 'name' => 'Jane Smith', 'email' => 'jane.smith@example.com', 'age' => 25, 'city' => 'Houston', 'created_at' => '2024-04-12 17:48:03'], ['id' => 5, 'name' => 'Alice Johnson', 'email' => 'alice.johnson@example.com', 'age' => 31, 'city' => 'Phoenix', 'created_at' => '2024-05-22 11:20:15'], ['id' => 6, 'name' => 'Bob Brown', 'email' => 'bob.brown@example.com', 'age' => 27, 'city' => 'Philadelphia', 'created_at' => '2024-06-30 13:35:49'], ['id' => 7, 'name' => 'Charlie Davis', 'email' => 'charlie.davis@example.com', 'age' => 36, 'city' => 'San Antonio', 'created_at' => '2024-07-15 16:10:05'], ['id' => 8, 'name' => 'Eve Wilson', 'email' => 'eve.wilson@example.com', 'age' => 28, 'city' => 'San Diego', 'created_at' => '2024-08-03 10:25:58'], ['id' => 9, 'name' => 'Frank Martin', 'email' => 'frank.martin@example.com', 'age' => 39, 'city' => 'Dallas', 'created_at' => '2024-09-08 19:42:31'], ['id' => 10, 'name' => 'Grace Lee', 'email' => 'grace.lee@example.com', 'age' => 22, 'city' => 'San Jose', 'created_at' => '2024-10-18 08:50:44'], ] as $item)
            <x-slate::table-row :even="$item['id'] % 2 === 0">
                <x-slate::table-cell>{{ $item['id'] }}</x-slate::table-cell>
                <x-slate::table-cell>{{ $item['name'] }}</x-slate::table-cell>
                <x-slate::table-cell align="center">
                    <button>Edit</button>
                    <button>Delete</button>
                </x-slate::table-cell>
            </x-slate::table-row>
        @endforeach
    </x-slate::table-body>
</x-slate::table>
@endverbatim
</x-code-preview>


## TableHeader Component

The `TableHeader` component wraps the table header row. You can customize the header's color.

### Props

| Prop   | Type   | Default  | Description                                          |
|--------|--------|----------|------------------------------------------------------|
| `color`| String | `'gray'` | Background color of the header. Supports any color.  |

### Usage Example

<x-code-preview>
@verbatim
<x-slate::table>
<x-slate::table-header color="gray">
    <x-slate::table-cell header>ID</x-slate::table-cell>
    <x-slate::table-cell header>Name</x-slate::table-cell>
    <x-slate::table-cell header align="center">Actions</x-slate::table-cell>
</x-slate::table-header>
</x-slate::table>
@endverbatim
</x-code-preview>


## TableBody Component

The `TableBody` component is a container for the main content of the table.

### Usage Example

<x-code-preview>
@verbatim
<x-slate::table>
<x-slate::table-body>
    @foreach([ ['id' => 1, 'name' => 'Lorem Ipsum', 'email' => 'lorem.ipsum@example.com', 'age' => 29, 'city' => 'New York', 'created_at' => '2024-01-15 08:23:45'], ['id' => 2, 'name' => 'Dolor Ismet', 'email' => 'dolor.ismet@example.com', 'age' => 34, 'city' => 'Los Angeles', 'created_at' => '2024-02-10 14:11:30'], ['id' => 3, 'name' => 'John Doe', 'email' => 'john.doe@example.com', 'age' => 40, 'city' => 'Chicago', 'created_at' => '2024-03-05 09:15:22'], ['id' => 4, 'name' => 'Jane Smith', 'email' => 'jane.smith@example.com', 'age' => 25, 'city' => 'Houston', 'created_at' => '2024-04-12 17:48:03'], ['id' => 5, 'name' => 'Alice Johnson', 'email' => 'alice.johnson@example.com', 'age' => 31, 'city' => 'Phoenix', 'created_at' => '2024-05-22 11:20:15'], ['id' => 6, 'name' => 'Bob Brown', 'email' => 'bob.brown@example.com', 'age' => 27, 'city' => 'Philadelphia', 'created_at' => '2024-06-30 13:35:49'], ['id' => 7, 'name' => 'Charlie Davis', 'email' => 'charlie.davis@example.com', 'age' => 36, 'city' => 'San Antonio', 'created_at' => '2024-07-15 16:10:05'], ['id' => 8, 'name' => 'Eve Wilson', 'email' => 'eve.wilson@example.com', 'age' => 28, 'city' => 'San Diego', 'created_at' => '2024-08-03 10:25:58'], ['id' => 9, 'name' => 'Frank Martin', 'email' => 'frank.martin@example.com', 'age' => 39, 'city' => 'Dallas', 'created_at' => '2024-09-08 19:42:31'], ['id' => 10, 'name' => 'Grace Lee', 'email' => 'grace.lee@example.com', 'age' => 22, 'city' => 'San Jose', 'created_at' => '2024-10-18 08:50:44'], ] as $item)
        <x-slate::table-row>
            <x-slate::table-cell>{{ $item['id'] }}</x-slate::table-cell>
            <x-slate::table-cell>{{ $item['name'] }}</x-slate::table-cell>
            <x-slate::table-cell align="center">
                <x-slate::button>Edit</x-slate::button>
                <x-slate::button>Delete</x-slate::button>
            </x-slate::table-cell>
        </x-slate::table-row>
    @endforeach
</x-slate::table-body>
</x-slate::table>
@endverbatim
</x-code-preview>


## TableRow Component

The `TableRow` component represents a single row in the table. It supports hover effects and striping.

### Props

| Prop       | Type    | Default  | Description                                                      |
|------------|---------|----------|------------------------------------------------------------------|
| `hoverable`| Boolean | `false`  | If `true`, the row is highlighted when hovered.                   |
| `striped`  | Boolean | `false`  | If `true`, applies background color for alternating striped rows. |
| `even`     | Boolean | `false`  | Indicates whether the row is even for striping purposes.          |

### Usage Example

<x-code-preview>
@verbatim
<x-slate::table>
<x-slate::table-row hoverable striped :even="true">
    <x-slate::table-cell>{{ 1 }}</x-slate::table-cell>
    <x-slate::table-cell>{{ 'Electrik Slate' }}</x-slate::table-cell>
    <x-slate::table-cell align="center">
        <button>Edit</button>
        <button>Delete</button>
    </x-slate::table-cell>
</x-slate::table-row>
</x-slate::table>
@endverbatim
</x-code-preview>


## TableCell Component

The `TableCell` component is used for individual cells within a row.

### Props

| Prop    | Type    | Default | Description                             |
|---------|---------|---------|-----------------------------------------|
| `header`| Boolean | `false` | If `true`, renders as a header cell (`th`). |
| `align` | String  | `'left'`| Text alignment. Options: `'left'`, `'center'`, `'right'`. |

### Usage Example

<x-code-preview>
@verbatim
<x-slate::table>
<x-slate::table-cell header align="center">Name</x-slate::table-cell>
<x-slate::table-cell align="right">{{ 'Electrik Slate' }}</x-slate::table-cell>
</x-slate::table>
@endverbatim
</x-code-preview>


## TableFooter Component

The `TableFooter` component is for the footer row of the table.

### Props

| Prop   | Type   | Default  | Description                                        |
|--------|--------|----------|----------------------------------------------------|
| `color`| String | `'gray'` | Background color of the footer. Supports any color. |

### Usage Example

<x-code-preview>
@verbatim
<x-slate::table>
<x-slate::table-footer color="blue">
    <x-slate::table-cell colspan="3" align="center">Footer Content</x-slate::table-cell>
</x-slate::table-footer>
</x-slate::table>
@endverbatim
</x-code-preview>
