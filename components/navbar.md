---
title: "Navbar"
description: "Learn how to use the Navbar component in Electrik Slate UI"
---

# Navbar

The `Navbar` component in Electrik Slate UI is a flexible navigation element that allows you to create responsive and customizable navigation bars. It supports dark mode and provides a clean, responsive design that adapts to various layouts.

## Props

| Prop Name    | Type    | Default | Description                                                                                              |
|--------------|---------|---------|----------------------------------------------------------------------------------------------------------|
| `attributes` | Array   | `[]`    | Additional classes or attributes to customize the navbar's appearance.                                    |

## Examples

### Basic Usage

The following example demonstrates a simple navbar with default styling:

<x-code-preview>
@verbatim
<x-slate::navbar>
    <x-slate::nav-item href="#">Home</x-slate::nav-item>
    <x-slate::nav-item href="#about">About</x-slate::nav-item>
    <x-slate::nav-item href="#contact">Contact</x-slate::nav-item>
</x-slate::navbar>
@endverbatim
</x-code-preview>

### Navbar with Dark Mode

This example shows how the navbar adapts to dark mode automatically. No extra configuration is needed:

<x-code-preview>
@verbatim
<x-slate::navbar>
    <x-slate::nav-item href="#">Dashboard</x-slate::nav-item>
    <x-slate::nav-item href="#settings">Settings</x-slate::nav-item>
    <x-slate::nav-item href="#profile">Profile</x-slate::nav-item>
</x-slate::navbar>
@endverbatim
</x-code-preview>

### Navbar with Custom Classes

You can customize the appearance of the navbar by adding additional classes:

<x-code-preview>
@verbatim
<x-slate::navbar class="bg-primary-500 text-white dark:bg-primary-700 dark:text-gray-100">
    <x-slate::nav-item href="#">Home</x-slate::nav-item>
    <x-slate::nav-item href="#services">Services</x-slate::nav-item>
    <x-slate::nav-item href="#contact">Contact</x-slate::nav-item>
</x-slate::navbar>
@endverbatim
</x-code-preview>

### Navbar with Brand and Menu Items

This example shows how to create a more complex navbar with a brand/logo on the left and navigation items on the right:

<x-code-preview>
@verbatim
<x-slate::navbar class="justify-between">
    <div class="flex items-center space-x-4">
        <x-slate::nav-item href="#">
            <x-slate::icon icon="carbon-flash-filled" />
        </x-slate::nav-item>
        <x-slate::nav-item href="#">Electrik</x-slate::nav-item>
    </div>
    <div class="flex space-x-8">
        <x-slate::nav-item href="#dashboard">Dashboard</x-slate::nav-item>
        <x-slate::nav-item href="#settings">Settings</x-slate::nav-item>
        <x-slate::nav-item href="#profile">Profile</x-slate::nav-item>
    </div>
</x-slate::navbar>
@endverbatim
</x-code-preview>

