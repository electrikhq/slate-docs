---
title: "Radio"
description: "Learn how to use the Radio component in Electrik Slate UI"
---

# Radio

The `Radio` component in Electrik Slate UI is a form element used to select a single option from a list of choices. It supports customization through props, integrates seamlessly with dark mode, and includes validation error messages.

## Props

| Prop Name  | Type    | Default | Description                                                                                          |
|------------|---------|---------|------------------------------------------------------------------------------------------------------|
| `name`     | String  | `null`  | The name of the radio input (required for form submissions).                                          |
| `value`    | String  | `null`  | The value of the radio input (required).                                                              |
| `checked`  | Boolean | `false` | Whether the radio input is checked by default.                                                        |
| `disabled` | Boolean | `false` | Whether the radio input is disabled.                                                                  |
| `label`    | String  | `null`  | The label text associated with the radio input.                                                       |
| `helpText` | String  | `null`  | Additional help text displayed below the label.                                                       |
| `error`    | String  | `null`  | Error message to be displayed below the radio input.                                                  |

## Examples

### Basic Radio Usage

This example demonstrates a basic radio input with a label:

<x-code-preview>
@verbatim
<!-- Basic Radio Input -->
<x-slate::radio name="example" value="option1" label="Option 1" />
@endverbatim
</x-code-preview>

### Checked Radio

This example demonstrates a radio input that is checked by default:

<x-code-preview>
@verbatim
<!-- Checked Radio Input -->
<x-slate::radio name="example" value="option2" label="Option 2" checked />
@endverbatim
</x-code-preview>

### Disabled Radio

This example demonstrates a radio input that is disabled:

<x-code-preview>
@verbatim
<!-- Disabled Radio Input -->
<x-slate::radio name="example" value="option3" label="Option 3" disabled />
@endverbatim
</x-code-preview>

### Radio with Error Message

This example demonstrates how to display an error message below the radio input:

<x-code-preview>
@verbatim
<!-- Radio Input with Error Message -->
<x-slate::radio 
    name="example" 
    value="option4" 
    label="Option 4" 
    error="You must select an option." 
/>
@endverbatim
</x-code-preview>

### Radio with Help Text

This example demonstrates how to display additional help text below the label:

<x-code-preview>
@verbatim
<!-- Radio Input with Help Text -->
<x-slate::radio 
    name="example" 
    value="option5" 
    label="Option 5" 
    helpText="This is additional information about the option." 
/>
@endverbatim
</x-code-preview>

### Radio in Dark Mode

This example demonstrates how the radio input adapts to dark mode:

<x-code-preview>
@verbatim
<!-- Radio Input in Dark Mode -->
<div class="dark">
    <x-slate::radio name="example" value="option6" label="Option 6" />
</div>
@endverbatim
</x-code-preview>

## Customization

The `Radio` component is flexible and easy to customize. It supports various states such as checked, disabled, and error. The `Radio` component's dark mode support ensures that it maintains readability across different themes.
