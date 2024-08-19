---
title: "Select"
description: "Learn how to use the Select component in Electrik Slate UI"
sidebar_order: 9
---

# Select

The `Select` component in Electrik Slate UI is a form element used to create dropdown menus for selecting an option or multiple options from a list. It supports customization through props, integrates seamlessly with dark mode, and includes validation error messages.

## Props

| Prop Name     | Type    | Default | Description                                                                                          |
|---------------|---------|---------|------------------------------------------------------------------------------------------------------|
| `label`       | String  | `null`  | The label text displayed above the select dropdown.                                                  |
| `name`        | String  | `''`    | The name attribute for the select input (required for form submissions).                             |
| `options`     | Array   | `[]`    | The options available in the select dropdown, passed as an associative array of value => display text. |
| `size`        | String  | `md`    | The size of the select element (`sm`, `md`, `lg`).                                                   |
| `placeholder` | String  | `null`  | An optional placeholder displayed as the first option (disabled and unselectable).                   |
| `disabled`    | Boolean | `false` | Whether the select dropdown is disabled.                                                             |
| `required`    | Boolean | `false` | Whether the select dropdown is required.                                                             |
| `multiple`    | Boolean | `false` | Whether to allow multiple selections.                                                                |
| `error`       | String  | `null`  | Error message to be displayed below the select dropdown.                                             |

## Examples

### Basic Select Usage

This example demonstrates a basic select dropdown with a label:

<x-code-preview>
@verbatim
<!-- Basic Select Input -->
<x-slate::select 
    label="Choose an option" 
    name="example" 
    :options="['option1' => 'Option 1', 'option2' => 'Option 2', 'option3' => 'Option 3']" 
/>
@endverbatim
</x-code-preview>

### Select with Placeholder

This example demonstrates a select dropdown with a placeholder:

<x-code-preview>
@verbatim
<!-- Select Input with Placeholder -->
<x-slate::select 
    label="Choose an option" 
    name="example" 
    placeholder="Select an option"
    :options="['option1' => 'Option 1', 'option2' => 'Option 2', 'option3' => 'Option 3']" 
/>
@endverbatim
</x-code-preview>

### Disabled Select

This example demonstrates a select dropdown that is disabled:

<x-code-preview>
@verbatim
<!-- Disabled Select Input -->
<x-slate::select 
    label="Choose an option" 
    name="example" 
    :options="['option1' => 'Option 1', 'option2' => 'Option 2']" 
    disabled
/>
@endverbatim
</x-code-preview>

### Multiple Select

This example demonstrates a select dropdown that allows multiple selections:

<x-code-preview>
@verbatim
<!-- Multiple Select Input -->
<x-slate::select 
    label="Choose options" 
    name="example" 
    :options="['option1' => 'Option 1', 'option2' => 'Option 2', 'option3' => 'Option 3']" 
    multiple
/>
@endverbatim
</x-code-preview>

### Select with Error Message

This example demonstrates how to display an error message below the select dropdown:

<x-code-preview>
@verbatim
<!-- Select Input with Error Message -->
<x-slate::select 
    label="Choose an option" 
    name="example" 
    :options="['option1' => 'Option 1', 'option2' => 'Option 2']" 
    error="This field is required."
/>
@endverbatim
</x-code-preview>

### Select in Dark Mode

This example demonstrates how the select dropdown adapts to dark mode:

<x-code-preview>
@verbatim
<!-- Select Input in Dark Mode -->
<div class="dark">
    <x-slate::select 
        label="Choose an option" 
        name="example" 
        :options="['option1' => 'Option 1', 'option2' => 'Option 2']" 
    />
</div>
@endverbatim
</x-code-preview>

## Customization

The `Select` component is flexible and easy to customize. It supports various states such as disabled, required, multiple selection, and error handling. The `Select` component's dark mode support ensures that it maintains readability across different themes.
