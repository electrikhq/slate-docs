---
title: "Checkboxes"
description: "Learn how to use the Checkbox component in Electrik Slate UI"
sidebar_order: 10
---

# Checkboxes

The `Checkbox` component in Electrik Slate UI is a versatile form control that allows users to select or deselect options. It supports various features like error messages, labels, help text, and disabled states.

## Props

| Prop Name  | Type    | Default  | Description                                                                                              |
|------------|---------|----------|----------------------------------------------------------------------------------------------------------|
| `name`     | String  | `null`   | The name attribute for the checkbox.                                                                      |
| `value`    | String  | `''`     | The value attribute for the checkbox.                                                                     |
| `checked`  | Boolean | `false`  | Whether the checkbox is checked by default.                                                               |
| `disabled` | Boolean | `false`  | Whether the checkbox is disabled.                                                                         |
| `label`    | String  | `null`   | An optional label to display next to the checkbox.                                                        |
| `helpText` | String  | `null`   | Additional help text to display below the label.                                                          |
| `error`    | String  | `null`   | An optional error message to display. If not provided, it will default to Laravel's validation errors.    |

## Examples

### Basic Usage

The following example demonstrates a simple checkbox with a label:

<x-code-preview>
@verbatim
<x-slate::checkbox name="subscribe" label="Subscribe to newsletter" />
@endverbatim
</x-code-preview>

### Checkbox with Error Message

This example shows a checkbox with an error message, which is automatically displayed when there's a validation error:

<x-code-preview>
@verbatim
<x-slate::checkbox name="terms" label="Accept Terms and Conditions" error="You must accept the terms and conditions." />
@endverbatim
</x-code-preview>

### Checkbox with Help Text

You can provide additional context to the user by including help text:

<x-code-preview>
@verbatim
<x-slate::checkbox name="updates" label="Receive updates" helpText="We'll send you the latest updates and promotions." />
@endverbatim
</x-code-preview>

### Disabled Checkbox

This example shows a checkbox that is disabled and cannot be interacted with:

<x-code-preview>
@verbatim
<x-slate::checkbox name="subscribe" label="Subscribe to newsletter" disabled />
@endverbatim
</x-code-preview>

### Checkbox with Dark Mode Support

This example demonstrates how the checkbox adapts to dark mode automatically:

<x-code-preview>
@verbatim
<x-slate::checkbox name="darkMode" label="Enable dark mode" checked />
@endverbatim
</x-code-preview>

## Customization

The `Checkbox` component is designed to be flexible and easy to customize. You can control its appearance and behavior to fit the needs of your application, whether it's for a simple form or a more complex UI.

### Handling Errors and Validation

The `Checkbox` component integrates seamlessly with Laravel's validation system. If there is a validation error for the checkbox, the error message will be displayed automatically, allowing you to ensure that users provide the correct input.
