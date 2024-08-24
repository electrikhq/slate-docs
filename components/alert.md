---
title: "Alerts"
description: "Learn how to use the Alert component in Electrik Slate UI"
---

# Alerts

The `Alert` component in Electrik Slate UI is a versatile notification element that allows users to display important messages or alerts. It supports various features like dark mode, customizable sizes, icons, dismissible alerts, and full-width styles.

## Props

| Prop Name    | Type    | Default | Description                                                                                              |
|--------------|---------|---------|----------------------------------------------------------------------------------------------------------|
| `size`       | String  | `md`    | The size of the alert (`sm`, `md`, `lg`).                                                                 |
| `dismissible`| Boolean | `false` | Whether the alert can be dismissed by the user.                                                           |
| `icon`       | String  | `null`  | An optional icon to display within the alert.                                                             |
| `color`      | String  | `blue`  | The color of the alert (`primary`, `secondary`, `success`, `danger`, `warning`, `info`, `black`, `white`).|
| `outlined`   | Boolean | `false` | Whether the alert should have an outlined style.                                                          |
| `full-width`  | Boolean | `false` | Whether the alert should span the full width of its container.                                            |

## Examples

### Basic Usage

The following example demonstrates a simple alert with a blue background and default size:

<x-code-preview>
@verbatim
<x-slate::alert>
    This is an default neutral alert.
</x-slate::alert>
<x-slate::alert outlined class="mt-4" size="sm" dismissible>
    This is an default outlined small dismissible alert.
</x-slate::alert>
<x-slate::alert class="mt-4" color="blue">
    This is an informational alert.
</x-slate::alert>
@endverbatim
</x-code-preview>

### Alert with Icon

This example shows how to use an icon within an alert:

<x-code-preview>
@verbatim
<x-slate::alert color="success" icon="carbon-checkmark">
    Operation completed successfully.
</x-slate::alert>
@endverbatim
</x-code-preview>

### Dismissible Alert

This example shows a dismissible alert that the user can close:

<x-code-preview>
@verbatim
<x-slate::alert color="danger" dismissible>
    There was an error processing your request.
</x-slate::alert>
@endverbatim
</x-code-preview>

### Outlined and Full-Width Alerts

You can create outlined and full-width alerts using the `outlined` and `fullWidth` props:

<x-code-preview>
@verbatim
<x-slate::alert color="warning" outlined>
    This is a warning alert with an outlined style.
</x-slate::alert>
<x-slate::alert color="info" full-width class="mt-4">
    This alert spans the full width of its container.
</x-slate::alert>
@endverbatim
</x-code-preview>

### Alerts with Black and White Modes

This example showcases alerts using explicit black and white modes, which adapt correctly to dark mode:

<x-code-preview>
@verbatim
<x-slate::alert color="black" size="lg" class="mb-4">
    This is a black alert.
</x-slate::alert>
<x-slate::alert color="white" size="lg" outlined>
    This is an outlined white alert.
</x-slate::alert>
@endverbatim
</x-code-preview>

## Customization

The `Alert` component is highly customizable, allowing you to control its appearance and behavior to fit the needs of your application. Whether you need a simple informational alert, a dismissible error message, or a full-width warning, the `Alert` component can accommodate your design requirements.

### Alert Sizes

You can control the size of the alert using the `size` prop:

- `sm` (Small)
- `md` (Medium, default)
- `lg` (Large)

Example:

<x-code-preview>
@verbatim
<x-slate::alert color="primary" size="sm" class="mb-4">
    Small alert message.
</x-slate::alert>
<x-slate::alert color="primary" size="lg">
    Large alert message.
</x-slate::alert>
@endverbatim
</x-code-preview>
