---
title: "Drawer"
description: "Learn how to use the Drawer component in Electrik Slate UI"
sidebar_order: 12
---

# Drawer

The `Drawer` component in Electrik Slate UI is a flexible and customizable sliding panel that can be used for navigation, sidebars, or additional content display. It supports various features like dark mode, customizable sizes, different positions, outlined styles, and a backdrop for improved user experience.

## Props

| Prop Name     | Type    | Default  | Description                                                                                              |
|---------------|---------|----------|----------------------------------------------------------------------------------------------------------|
| `size`        | String  | `md`     | The size of the drawer (`sm`, `md`, `lg`).                                                                |
| `color`       | String  | `white`  | The background color of the drawer (`black`, `white`, or any other Tailwind color).                       |
| `outlined`    | Boolean | `false`  | Whether the drawer should have an outlined style.                                                         |
| `position`    | String  | `left`   | The position of the drawer (`left`, `right`, `top`, `bottom`).                                            |
| `header`      | String  | `null`   | Optional header content for the drawer.                                                                   |
| `footer`      | String  | `null`   | Optional footer content for the drawer.                                                                   |
| `toggleButton`| String  | `null`   | Slot for the button that toggles the drawer open and closed.                                              |

## Examples

### Drawer Sliding in from the Top

This example demonstrates a drawer that slides in from the top with a custom toggle button, a header, and a footer:

<x-code-preview>
@verbatim
<!-- Drawer with custom toggle button, no borders, sliding in from the top -->
<x-slate::drawer size="md" color="white" position="top">
    <x-slot name="toggleButton">
        <button class="px-4 py-2 bg-blue-500 text-white rounded">Toggle Top Drawer</button>
    </x-slot>
    <x-slot name="header">
        Custom Drawer Header
    </x-slot>
    <x-slot name="footer">
        Custom Drawer Footer
    </x-slot>
    This is the main content of the drawer.
</x-slate::drawer>
@endverbatim
</x-code-preview>

### Drawer Sliding in from the Left

This example shows a drawer that slides in from the left, with a custom toggle button, a header, and a footer:

<x-code-preview>
@verbatim
<!-- Drawer with custom toggle button, no borders, sliding in from the left -->
<x-slate::drawer size="md" color="white">
    <x-slot name="toggleButton">
        <button class="px-4 py-2 bg-blue-500 text-white rounded">Toggle Left Drawer</button>
    </x-slot>
    <x-slot name="header">
        Custom Drawer Header
    </x-slot>
    <x-slot name="footer">
        Custom Drawer Footer
    </x-slot>
    This is the main content of the drawer.
</x-slate::drawer>
@endverbatim
</x-code-preview>

### Drawer with Backdrop Sliding in from the Left

This example shows a drawer with a backdrop that slides in from the left:

<x-code-preview>
@verbatim
<!-- Drawer with custom toggle button and backdrop, sliding in from the left -->
<x-slate::drawer size="md" color="white">
    <x-slot name="toggleButton">
        <button class="px-4 py-2 bg-blue-500 text-white rounded">Toggle Drawer with Backdrop</button>
    </x-slot>
    <x-slot name="header">
        Drawer with Backdrop Header
    </x-slot>
    <x-slot name="footer">
        Drawer with Backdrop Footer
    </x-slot>
    This is the main content of the drawer.
</x-slate::drawer>
@endverbatim
</x-code-preview>

### Outlined Black Drawer Sliding in from the Right

This example shows an outlined black drawer that slides in from the right, with a custom toggle button, a header, and a footer:

<x-code-preview>
@verbatim
<!-- Outlined black drawer with a footer, sliding in from the right with backdrop -->
<x-slate::drawer size="lg" color="black" outlined position="right">
    <x-slot name="toggleButton">
        <button class="px-4 py-2 bg-black text-white rounded">Toggle Right Drawer</button>
    </x-slot>
    <x-slot name="header">
        Right Drawer Header
    </x-slot>
    <x-slot name="footer">
        Right Drawer Footer
    </x-slot>
    This is the main content of the drawer.
</x-slate::drawer>
@endverbatim
</x-code-preview>

## Customization

The `Drawer` component is highly customizable, allowing you to control its appearance and behavior to fit the needs of your application. Whether you need a simple sidebar, a modal-like drawer with a backdrop, or a sliding panel from any direction, the `Drawer` component can accommodate your design requirements.
