---
title: "Icon"
description: "Learn how to use the Icon component in Electrik Slate UI"
sidebar_order: 5
---

# Icon

The `Icon` component in Electrik Slate UI allows you to easily include scalable vector icons in your application. With support for dark mode, customizable sizes, and color options, it integrates seamlessly into your design system.

## Props

| Prop Name  | Type   | Default       | Description                                                                                                     |
|------------|--------|---------------|-----------------------------------------------------------------------------------------------------------------|
| `icon`     | String | `null`        | The name of the icon to display (required).                                                                     |
| `size`     | String | `md`          | The size of the icon (`xs`, `sm`, `md`, `lg`, `xl`).                                                             |
| `color`    | String | `currentColor`| The color of the icon (inheriting from parent by default, or using a Tailwind color class).                      |
| `darkColor`| String | `white`       | The color of the icon when in dark mode (defaults to white if `color` is `currentColor`).                        |
| `class`    | String | `''`          | Additional classes to apply to the icon component.                                                              |

## Examples

### Basic Icon Usage

This example demonstrates how to use an icon with default settings:

<x-code-preview>
@verbatim
<!-- Basic Icon -->
<x-slate::icon icon="carbon-checkmark" />
@endverbatim
</x-code-preview>

### Custom Icon Size

This example demonstrates how to use an icon with a custom size:

<x-code-preview>
@verbatim
<!-- Icon with custom size -->
<x-slate::icon icon="carbon-checkmark" size="lg" />
<!-- Icon with custom size -->
<x-slate::icon icon="carbon-checkmark" size="sm" />
<!-- Icon with custom size -->
<x-slate::icon icon="carbon-checkmark" size="xs" />
@endverbatim
</x-code-preview>

### Custom Icon Color

This example demonstrates how to use an icon with a custom color:

<x-code-preview>
@verbatim
<!-- Icon with custom color -->
<x-slate::icon icon="carbon-checkmark" color="primary" />
@endverbatim
</x-code-preview>

### Icon with Dark Mode Support

This example demonstrates how the icon adapts to dark mode, changing its color based on the `darkColor` prop:

<x-code-preview>
@verbatim
<!-- Icon with dark mode support -->
<x-slate::icon icon="carbon-checkmark" color="gray-800" darkColor="white" />
@endverbatim
</x-code-preview>

### Custom Classes

This example demonstrates how to apply additional custom classes to the icon:

<x-code-preview>
@verbatim
<!-- Icon with custom classes -->
<x-slate::icon icon="carbon-checkmark" class="animate-spin" />
@endverbatim
</x-code-preview>

## Customization

The `Icon` component is highly customizable, allowing you to control its size, color, and behavior to fit the needs of your application. By default, it inherits the color from its parent element, but you can easily override this with specific colors or dark mode adjustments.