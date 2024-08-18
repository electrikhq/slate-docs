---
title: "Buttons"
description: "Learn how to use the Button component in Electrik Slate UI"
sidebar_order: 2
---

# Buttons

The `Button` component in Electrik Slate UI is a versatile and customizable element that allows users to trigger actions or navigate between pages. It supports various features like dark mode, customizable sizes, icons, rounded corners, and loading states.

## Props

| Prop Name      | Type    | Default | Description                                                                                               |
|----------------|---------|---------|-----------------------------------------------------------------------------------------------------------|
| `type`         | String  | `button`| The type of the button (`button`, `submit`, `reset`).                                                      |
| `color`        | String  | `black` | The color of the button (`primary`, `secondary`, `success`, `danger`, `warning`, `info`, `black`, `white`).|
| `size`         | String  | `md`    | The size of the button (`sm`, `md`, `lg`, `xl`).                                                           |
| `outlined`     | Boolean | `false` | Whether the button is outlined.                                                                            |
| `rounded`      | Boolean | `false` | Whether the button has fully rounded corners.                                                              |
| `disabled`     | Boolean | `false` | Whether the button is disabled.                                                                            |
| `href`         | String  | `null`  | The URL to navigate to if the button is used as a link.                                                    |
| `icon`         | String  | `null`  | An optional icon to display within the button.                                                             |
| `iconPosition` | String  | `prefix`| The position of the icon relative to the text (`prefix`, `suffix`).                                        |
| `loading`      | Boolean | `false` | Whether the button is in a loading state, displaying a spinner icon.                                       |

## Examples

### Basic Usage

The following example demonstrates a simple button with primary color and default size:

<x-code-preview>
@verbatim
<x-slate::button color="primary" size="md">
    Primary Button
</x-slate::button>
@endverbatim
</x-code-preview>

### Button with Icon

This example shows how to use an icon within a button. The icon is placed before the text by default.

<x-code-preview>
@verbatim
<x-slate::button color="success" icon="carbon-checkmark">
    Success
</x-slate::button>
@endverbatim
</x-code-preview>

You can also position the icon after the text using the `iconPosition` prop:

<x-code-preview>
@verbatim
<x-slate::button color="info" icon="carbon-information" iconPosition="suffix">
    More Info
</x-slate::button>
@endverbatim
</x-code-preview>

### Button with Loading State

This example shows a button in a loading state, displaying a spinner icon:

<x-code-preview>
@verbatim
<x-slate::button color="warning" loading>
    Loading...
</x-slate::button>
@endverbatim
</x-code-preview>

### Outlined and Rounded Buttons

You can create outlined and rounded buttons using the `outlined` and `rounded` props:

<x-code-preview>
@verbatim
<x-slate::button color="danger" outlined rounded>
    Rounded Outlined Button
</x-slate::button>
@endverbatim
</x-code-preview>

### Buttons with Black and White Modes

This example showcases buttons using explicit black and white modes, which adapt correctly to dark mode:

<x-code-preview>
@verbatim
<x-slate::button color="black" size="lg">
    Black Button
</x-slate::button>

<x-slate::button color="white" size="lg">
    White Button
</x-slate::button>
@endverbatim
</x-code-preview>

### Disabled Button

This example shows a button that is disabled:

<x-code-preview>
@verbatim
<x-slate::button color="secondary" disabled>
    Disabled Button
</x-slate::button>
@endverbatim
</x-code-preview>

## Customization

The `Button` component is highly customizable, allowing you to control its appearance and behavior to fit the needs of your application. Whether you need a simple action button, a navigation link, or a complex button with icons and loading states, the `Button` component can accommodate your design requirements.

### Button Sizes

You can control the size of the button using the `size` prop:

- `sm` (Small)
- `md` (Medium, default)
- `lg` (Large)
- `xl` (Extra Large)

Example:

<x-code-preview>
@verbatim
<x-slate::button color="primary" size="sm">
    Small Button
</x-slate::button>
<x-slate::button color="primary" size="lg">
    Large Button
</x-slate::button>
<x-slate::button color="primary" size="xl">
    Extra Large Button
</x-slate::button>
@endverbatim
</x-code-preview>
