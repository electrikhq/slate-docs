---
title: "Toggle"
description: "Learn how to use the Toggle component in Electrik Slate UI"
sidebar_order: 10
---

# Toggle

The `Toggle` component in Electrik Slate UI is a form element that allows users to switch between two states, such as on/off or true/false. It supports customization through props, integrates seamlessly with dark mode, and includes validation error messages.

## Props

| Prop Name  | Type    | Default | Description                                                                                          |
|------------|---------|---------|------------------------------------------------------------------------------------------------------|
| `name`     | String  | `toggle`| The name attribute for the toggle input (required for form submissions).                             |
| `checked`  | Boolean | `false` | Whether the toggle input is checked by default.                                                      |
| `disabled` | Boolean | `false` | Whether the toggle input is disabled.                                                                |
| `size`     | String  | `md`    | The size of the toggle input (`sm`, `md`, `lg`).                                                     |
| `color`    | String  | `black` | The color of the toggle when it is checked.                                                          |
| `label`    | String  | `null`  | The label text associated with the toggle input.                                                     |
| `error`    | String  | `null`  | Error message to be displayed below the toggle input.                                                |
| `helpText` | String  | `null`  | Additional help text displayed below the label.                                                      |
| `value`    | String  | `''`    | The value attribute for the toggle input.                                                            |

## Examples

### Basic Toggle Usage

This example demonstrates a basic toggle input with a label:

<x-code-preview>
@verbatim
<!-- Basic Toggle Input -->
<x-slate::toggle name="exampleToggle" label="Enable Feature" />
@endverbatim
</x-code-preview>

### Checked Toggle

This example demonstrates a toggle input that is checked by default:

<x-code-preview>
@verbatim
<!-- Checked Toggle Input -->
<x-slate::toggle name="checkedToggle" label="Enable Feature" checked />
@endverbatim
</x-code-preview>

### Disabled Toggle

This example demonstrates a toggle input that is disabled:

<x-code-preview>
@verbatim
<!-- Disabled Toggle Input -->
<x-slate::toggle name="disabledToggle" label="Enable Feature" disabled />
@endverbatim
</x-code-preview>

### Toggle with Error Message

This example demonstrates how to display an error message below the toggle input:

<x-code-preview>
@verbatim
<!-- Toggle Input with Error Message -->
<x-slate::toggle 
    name="errorToggle" 
    label="Enable Feature" 
    error="This field is required." 
/>
@endverbatim
</x-code-preview>

### Toggle with Help Text

This example demonstrates how to display additional help text below the label:

<x-code-preview>
@verbatim
<!-- Toggle Input with Help Text -->
<x-slate::toggle 
    name="helpToggle" 
    label="Enable Feature" 
    helpText="This is additional information about the toggle." 
/>
@endverbatim
</x-code-preview>

### Toggle in Dark Mode

This example demonstrates how the toggle input adapts to dark mode:

<x-code-preview>
@verbatim
<!-- Toggle Input in Dark Mode -->
<div class="dark">
    <x-slate::toggle name="darkModeToggle" label="Enable Feature" />
</div>
@endverbatim
</x-code-preview>

### Custom Toggle Size and Color

This example demonstrates a toggle with custom size and color:

<x-code-preview>
@verbatim
<!-- Custom Toggle Size and Color -->
<x-slate::toggle name="customToggle" label="Enable Feature" size="lg" color="blue" />
@endverbatim
</x-code-preview>

## Customization

The `Toggle` component is flexible and easy to customize. It supports various states such as checked, disabled, and error. The `Toggle` component's dark mode support ensures that it maintains readability across different themes.
