---
title: "Status"
description: "Learn how to use the Status component in Slate UI"
sidebar_order: 10
---

# Status

The `Status` component is a versatile indicator for various statuses across your application. It is customizable in terms of size, color, and style, making it adaptable to different UI needs.

## Props

| Prop       | Type      | Default    | Description                                                                                   |
|------------|-----------|------------|-----------------------------------------------------------------------------------------------|
| `size`     | `string`  | `md`       | Defines the size of the status. Options: `xs`, `sm`, `md`, `lg`, `xl`.                    |
| `color`    | `string`  | `green`    | Sets the color of the status. Supports Tailwind colors and handles `black` and `white` explicitly. |
| `outlined` | `boolean` | `false`    | If `true`, renders the status with only a border and no fill.                             |
| `label`    | `string`  | `null`     | An optional label to be displayed next to the status.                                     |

## Examples

### Default Status

A basic Status with the default settings.

<x-code-preview>
@verbatim
<x-slate::status color="green" />
@endverbatim
</x-code-preview>

### Status with Label

Add a label next to the Status to provide context.

<x-code-preview>
@verbatim
<x-slate::status color="red" size="lg" label="Offline" />
@endverbatim
</x-code-preview>

### Outlined Status

Use the `outlined` prop to create a bordered Status without fill.

<x-code-preview>
@verbatim
<x-slate::status color="blue" outlined size="sm" label="In Progress" />
@endverbatim
</x-code-preview>

### Status with Black Color

Explicit handling for black color, ensuring correct styling in light and dark modes.

<x-code-preview>
@verbatim
<x-slate::status color="black" size="md" label="Busy" />
@endverbatim
</x-code-preview>

### Status with White Color

Explicit handling for white color, ensuring correct styling in light and dark modes.

<x-code-preview>
@verbatim
<x-slate::status color="white" size="md" label="Available" />
@endverbatim
</x-code-preview>

### Statuss in Different Sizes and Styles

Showcase different sizes and styles of Statuss.

<x-code-preview>
@verbatim
<x-slate::status color="green" size="xs" label="Small" />
<x-slate::status color="yellow" size="sm" label="Warning" />
<x-slate::status color="blue" size="md" label="Normal" />
<x-slate::status color="red" size="lg" label="Error" />
<x-slate::status color="black" size="xl" label="Critical" />
@endverbatim
</x-code-preview>
