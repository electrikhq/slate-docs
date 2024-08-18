---
title: "Dropdown"
description: "Learn how to use the Dropdown component in Electrik Slate UI"
sidebar_order: 4
---

# Dropdown

The `Dropdown` component in Electrik Slate UI is a versatile and customizable component that allows users to display a list of actions or options in a dropdown menu. It supports various features like dark mode, customizable sizes, icons, and flexible positioning.

## Props

| Prop Name  | Type   | Default | Description                                                                 |
|------------|--------|---------|-----------------------------------------------------------------------------|
| `label`    | String | `null`  | The label for the dropdown trigger button.                                  |
| `size`     | String | `md`    | The size of the dropdown (`sm`, `md`, `lg`).                                |
| `color`    | String | `primary`| The color of the dropdown trigger button (`primary`, `secondary`, `black`, `white`, etc.). |
| `icon`     | String | `null`  | An optional icon for the dropdown trigger button.                           |
| `position` | String | `bottom-right` | Position of the dropdown menu (`bottom-right`, `bottom-left`, `top-right`, `top-left`). |
| `disabled` | Boolean| `false` | Whether the dropdown is disabled.                                           |

## Examples

### Basic Usage

The following example demonstrates a simple dropdown with a primary-colored trigger button and a list of actions.

<x-code-preview>
@verbatim
<x-slate::dropdown label="Actions" icon="carbon-settings" color="primary" size="md">
    <x-slate::dropdown-item label="Edit" icon="carbon-edit" />
    <x-slate::dropdown-item label="Delete" icon="carbon-trash-can" />
</x-slate::dropdown>
@endverbatim
</x-code-preview>

### Dropdown with Black and White Modes

This example showcases dropdowns using explicit black and white modes, which adapt correctly to dark mode:

<x-code-preview>
@verbatim
<x-slate::dropdown label="Settings" icon="carbon-settings" color="black" size="md">
    <x-slate::dropdown-item label="Profile" icon="carbon-user-avatar" />
    <x-slate::dropdown-item label="Logout" icon="carbon-logout" />
</x-slate::dropdown>
<x-slate::dropdown label="Options" icon="carbon-overflow-menu-horizontal" color="white" size="md">
    <x-slate::dropdown-item label="Settings" icon="carbon-settings-adjust" />
    <x-slate::dropdown-item label="Help" icon="carbon-help" />
</x-slate::dropdown>
@endverbatim
</x-code-preview>

### Dropdown with Descriptions

In this example, each dropdown item includes a description, providing additional context for the options:

<x-code-preview>
@verbatim
<x-slate::dropdown label="More Options" icon="carbon-overflow-menu-horizontal" color="secondary" size="lg">
    <x-slate::dropdown-item label="Profile" icon="carbon-user-avatar" description="View and edit your profile" />
    <x-slate::dropdown-item label="Settings" icon="carbon-settings-adjust" description="Adjust your preferences" />
    <x-slate::dropdown-item label="Logout" icon="carbon-logout" description="Sign out of your account" />
</x-slate::dropdown>
@endverbatim
</x-code-preview>

### Disabled Dropdown

This example shows a dropdown that is disabled:

<x-code-preview>
@verbatim
<x-slate::dropdown label="Disabled Dropdown" icon="carbon-close-outline" color="danger" size="md" disabled>
    <x-slate::dropdown-item label="Option 1" />
    <x-slate::dropdown-item label="Option 2" />
</x-slate::dropdown>
@endverbatim
</x-code-preview>

## Customization

The `Dropdown` component is highly customizable. You can adjust its size, color, and position to fit the needs of your application. Whether you need a simple dropdown for basic actions or a more complex one with descriptions and icons, the `Dropdown` component can accommodate your design requirements.

### Positioning

You can control where the dropdown menu appears relative to the trigger button using the `position` prop:

- `bottom-right` (default)
- `bottom-left`
- `top-right`
- `top-left`

Example:

<x-code-preview>
@verbatim
<x-slate::dropdown label="Top Left" icon="carbon-settings" color="primary" size="md" position="top-left">
    <x-slate::dropdown-item label="Edit" />
    <x-slate::dropdown-item label="Delete" />
</x-slate::dropdown>
@endverbatim
</x-code-preview>

