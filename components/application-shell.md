---
title: "Appliction Shell"
description: "Get started with Slate"
sidebar_order: 1
---

# Shell Component

The `Shell` component is a flexible layout container that provides a primary sidebar, secondary sidebar, top navigation bar, and main content area. It is designed to structure your application's layout in a consistent and reusable manner, supporting both light and dark modes.

## Props

| Prop Name         | Type     | Default    | Description                                                                                  |
|-------------------|----------|------------|----------------------------------------------------------------------------------------------|
| `primarySidebar`  | Slot     | `null`     | Content for the primary sidebar, usually containing navigation icons or links.               |
| `sidebar`         | Slot     | `null`     | Content for the secondary sidebar, typically containing links or additional navigation.       |
| `navbar`          | Slot     | `null`     | Content for the top navigation bar, typically containing navigation links or buttons.         |
| `slot`            | Slot     | `null`     | The main content area, where the core content of the page is displayed.                      |

## Examples

### Basic Usage

Here's a basic example of how to use the `Shell` component with a primary sidebar, secondary sidebar, and main content area.

<x-code-preview>
@verbatim
<x-slate::shell>
    <x-slot name="primarySidebar">
        <!-- Primary Sidebar content for preview -->
        <x-slate::icon icon="carbon-dashboard" size="md" class="hover:text-gray-700 cursor-pointer" />
    </x-slot>
    <x-slot name="sidebar">
        <div class="px-5">
            <!-- Secondary Sidebar content for preview -->
            <x-slate::button size="xs">Sidebar Button</x-slate::button>
        </div>
    </x-slot>
    <x-slot name="navbar">
        <!-- Navbar content for preview -->
        <x-slate::navbar>
            <x-slate::nav-item>Dashboard</x-slate::nav-item>
            <x-slate::nav-item>Profile</x-slate::nav-item>
        </x-slate::navbar>
    </x-slot>
    <!-- Main content for preview -->
    <div class="p-4">
        <h1 class="text-lg font-bold">Main Content</h1>
        <p>This is an example of the main content area within the shell component.</p>
    </div>
</x-slate::shell>
@endverbatim
</x-code-preview>


### Advanced Usage with Sidebar Toggle

In this example, the secondary sidebar can be toggled using a button in the top navigation bar.

<x-code-preview>
@verbatim
<x-slate::shell>
    <x-slot name="primarySidebar">
        <!-- Primary Sidebar content -->
        <x-slate::icon icon="carbon-dashboard" size="md" class="hover:text-gray-700 cursor-pointer" />
    </x-slot>
    <x-slot name="sidebar">
        <div class="px-5">
            <!-- Secondary Sidebar content -->
            <a href="#" onclick="return false">Settings</a><br/>
            <a href="#" onclick="return false">Profile</a>
        </div>
    </x-slot>
    <x-slot name="navbar">
        <!-- Navbar with toggle button -->
        <x-slate::navbar>
            <x-slate::nav-item>
                <x-slate::sidebar-toggle />
            </x-slate::nav-item>
            <x-slate::nav-item>Dashboard</x-slate::nav-item>
            <x-slate::nav-item>Profile</x-slate::nav-item>
        </x-slate::navbar>
    </x-slot>
    <!-- Main content -->
    <div class="p-4">
        <h1 class="text-lg font-bold">Main Content Area</h1>
        <p>This content is part of the main section of the page.</p>
    </div>
</x-slate::shell>
@endverbatim
</x-code-preview>

## Customization

The `Shell` component is highly customizable. You can use slots to define the content of the primary sidebar, secondary sidebar, and top navigation bar. The main content area can be populated with any content or components needed for your page.