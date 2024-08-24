---
title: "Input"
description: "Learn how to use the Input component in Electrik Slate UI"
---


# Input

The `Input` component in Electrik Slate UI is a versatile and customizable form element that supports various types, sizes, and styles. It comes with built-in support for dark mode, validation error messages, and additional elements like prefixes and suffixes.

## Props

| Prop Name   | Type    | Default  | Description                                                                                          |
|-------------|---------|----------|------------------------------------------------------------------------------------------------------|
| `type`      | String  | `text`   | The type of the input field (e.g., `text`, `email`, `password`, etc.).                                |
| `label`     | String  | `null`   | The label text associated with the input field.                                                       |
| `id`        | String  | `null`   | The ID of the input field. If not provided, it defaults to the name.                                  |
| `name`      | String  | `null`   | The name of the input field (required for form submissions).                                          |
| `value`     | String  | `''`     | The default value of the input field.                                                                 |
| `placeholder`| String | `''`     | The placeholder text for the input field.                                                             |
| `required`  | Boolean | `false`  | Whether the input field is required.                                                                  |
| `readonly`  | Boolean | `false`  | Whether the input field is read-only.                                                                 |
| `disabled`  | Boolean | `false`  | Whether the input field is disabled.                                                                  |
| `helpText`  | String  | `null`   | Additional help text displayed below the input field.                                                 |
| `error`     | String  | `null`   | Error message to be displayed below the input field.                                                  |
| `size`      | String  | `md`     | The size of the input field (`sm`, `md`, `lg`, `xl`).                                                 |
| `before`    | String  | `null`   | Content to be displayed as a prefix inside the input field (e.g., an icon or text).                   |
| `after`    | String  | `null`   | Content to be displayed as a suffix inside the input field (e.g., an icon or text).                   |

## Examples

### Basic Input Usage

This example demonstrates a simple text input with a label:

<x-code-preview>
@verbatim
<!-- Basic Input with Label -->
<x-slate::input name="email" label="Email Address" placeholder="Enter your email" />
@endverbatim
</x-code-preview>

### Input with Error Message

This example demonstrates how to display an error message below the input field:

<x-code-preview>
@verbatim
<!-- Input with Error Message -->
<x-slate::input 
    name="email" 
    label="Email Address" 
    placeholder="Enter your email" 
    error="Please enter a valid email address." 
/>
@endverbatim
</x-code-preview>

### Input with Prefix and Suffix

This example demonstrates how to use a prefix and suffix with the input field:

<x-code-preview>
@verbatim
<!-- Input with Prefix and Suffix -->
<x-slate::input 
    name="username" 
    label="Username" 
    placeholder="Enter your username" 
    before="@" 
    after=".com" 
/>
@endverbatim
</x-code-preview>

### Required Input
This example demonstrates how to make an input field required:

<x-code-preview>
@verbatim
<!-- Required Input -->
<x-slate::input 
    name="email" 
    label="Email Address" 
    placeholder="Enter your email" 
    required 
/>
@endverbatim
</x-code-preview>

### Disabled Input
This example demonstrates how to disable an input field:

<x-code-preview>
@verbatim
<!-- Disabled Input -->
<x-slate::input 
    name="email" 
    label="Email Address" 
    placeholder="Enter your email" 
    disabled 
/>
@endverbatim
</x-code-preview>

### Input with Custom Size

This example demonstrates how to use different sizes for the input field:

<x-code-preview>
@verbatim
<!-- Input with Custom Size -->
<x-slate::input name="password" label="Password" type="password" size="lg" placeholder="Enter your password" />
<!-- Input with Custom Size -->
<x-slate::input name="password" label="Password" type="password" size="sm" placeholder="Enter your password" />
@endverbatim
</x-code-preview>

### Input with Help Text

This example demonstrates how to display additional help text below the input field:

<x-code-preview>
@verbatim
<!-- Input with Help Text -->
<x-slate::input 
    name="email" 
    label="Email Address" 
    placeholder="Enter your email" 
    helpText="We'll never share your email with anyone else." 
/>
@endverbatim
</x-code-preview>

## Customization

The `Input` component is highly customizable, allowing you to control its size, style, and behavior to fit the needs of your application. Whether you're creating a simple form or a complex UI, the `Input` component adapts to your requirements with ease.