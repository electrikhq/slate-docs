---
title: "Badges"
description: "Learn how to use the Badge component in Electrik Slate UI"
sidebar_order: 7
---

# Badges

The `Badge` component in Electrik Slate UI is a flexible and customizable element that allows users to display labels, counts, or status indicators. It supports various features like dark mode, customizable sizes, icons, and outlined styles.

## Props

| Prop Name  | Type    | Default | Description                                                                                              |
|------------|---------|---------|----------------------------------------------------------------------------------------------------------|
| `color`    | String  | `primary` | The color of the badge (`primary`, `secondary`, `success`, `danger`, `warning`, `info`, `black`, `white`).|
| `size`     | String  | `md`     | The size of the badge (`xs`, `sm`, `md`, `lg`).                                                          |
| `icon`     | String  | `null`   | An optional icon to display inside the badge.                                                            |
| `text`     | String  | `null`   | The text or number to display inside the badge.                                                          |
| `outlined` | Boolean | `false`  | Whether the badge should have an outlined style.                                                         |

## Examples

### Basic Usage

The following example demonstrates a simple badge with a primary background and default size:

<x-code-preview>
@verbatim
<x-slate::badge color="primary">
    New
</x-slate::badge>
@endverbatim
</x-code-preview>

### Badge with Icon

This example shows how to use an icon within a badge:

<x-code-preview>
@verbatim
<x-slate::badge color="success" icon="carbon-checkmark">
    Success
</x-slate::badge>
@endverbatim
</x-code-preview>

### Outlined Badge

This example shows a badge with an outlined style:

<x-code-preview>
@verbatim
<x-slate::badge color="danger" outlined>
    Danger
</x-slate::badge>
@endverbatim
</x-code-preview>

### Badge with Black and White Modes

This example showcases badges using explicit black and white modes, which adapt correctly to dark mode:

<x-code-preview>
@verbatim
<x-slate::badge color="black" size="lg">
    Black Badge
</x-slate::badge>
<x-slate::badge color="white" size="lg" outlined>
    White Badge
</x-slate::badge>
@endverbatim
</x-code-preview>

### Customizing Badge Size

You can control the size of the badge using the `size` prop:

<x-code-preview>
@verbatim
<x-slate::badge color="secondary" size="xs">
    XS Badge
</x-slate::badge>
<x-slate::badge color="secondary" size="sm">
    Small Badge
</x-slate::badge>
<x-slate::badge color="secondary" size="lg">
    Large Badge
</x-slate::badge>
@endverbatim
</x-code-preview>

### Badge with Icon and Outlined Style

This example combines both an icon and outlined style in a badge:

<x-code-preview>
@verbatim
<x-slate::badge color="info" icon="carbon-information" outlined>
    Info
</x-slate::badge>
@endverbatim
</x-code-preview>

## Customization

The `Badge` component is highly customizable, allowing you to control its appearance and behavior to fit the needs of your application. Whether you need a simple label, a status indicator with an icon, or an outlined badge for emphasis, the `Badge` component can accommodate your design requirements.
