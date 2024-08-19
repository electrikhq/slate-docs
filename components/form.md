---
title: "Form"
description: "Learn how to use the Form component in Electrik Slate UI"
sidebar_order: 10
---

# Form

The `Form` component in Electrik Slate UI provides a flexible and customizable way to structure and style forms in your application. With built-in support for dark mode and easy customization options, it can be used to create forms with consistent spacing and layout.

## Props

| Prop Name      | Type    | Default | Description                                                           |
|----------------|---------|---------|-----------------------------------------------------------------------|
| `attributes`   | Array   | `null`  | Additional attributes to apply to the form element (e.g., `action`, `method`). |
| `slot`         | Slot    | `null`  | Content of the form, including form fields, buttons, etc.             |

## Examples

### Basic Form Usage

This example demonstrates a simple form with default styling:

<x-code-preview>
@verbatim
<!-- Basic Form -->
<x-slate::form action="/submit" method="POST">
    <div>
        <label for="email" class="block text-sm font-medium text-gray-700">Email address</label>
        <input type="email" name="email" id="email" required class="mt-1 block w-full rounded-md border-gray-300 shadow-sm focus:border-indigo-500 focus:ring-indigo-500 sm:text-sm">
    </div>
    <div>
        <label for="password" class="block text-sm font-medium text-gray-700">Password</label>
        <input type="password" name="password" id="password" required class="mt-1 block w-full rounded-md border-gray-300 shadow-sm focus:border-indigo-500 focus:ring-indigo-500 sm:text-sm">
    </div>
    <div>
        <button type="submit" class="px-4 py-2 bg-blue-500 text-white rounded-md">Submit</button>
    </div>
</x-slate::form>
@endverbatim
</x-code-preview>

### Form with Additional Attributes

This example demonstrates a form that includes additional attributes like `action` and `method`:

<x-code-preview>
@verbatim
<!-- Form with Additional Attributes -->
<x-slate::form action="/login" method="POST" class="space-y-6">
    <div>
        <label for="username" class="block text-sm font-medium text-gray-700">Username</label>
        <input type="text" name="username" id="username" required class="mt-1 block w-full rounded-md border-gray-300 shadow-sm focus:border-indigo-500 focus:ring-indigo-500 sm:text-sm">
    </div>
    <div>
        <label for="password" class="block text-sm font-medium text-gray-700">Password</label>
        <input type="password" name="password" id="password" required class="mt-1 block w-full rounded-md border-gray-300 shadow-sm focus:border-indigo-500 focus:ring-indigo-500 sm:text-sm">
    </div>
    <div>
        <button type="submit" class="px-4 py-2 bg-green-500 text-white rounded-md">Login</button>
    </div>
</x-slate::form>
@endverbatim
</x-code-preview>

### Form with Slots

This example demonstrates how to use slots within the form to include various elements like inputs, buttons, and additional content:

<x-code-preview>
@verbatim
<!-- Form with Slots -->
<x-slate::form>
    <x-slot name="header">
        <h3 class="text-lg leading-6 font-medium text-gray-900">Sign in to your account</h3>
    </x-slot>
    <div>
        <label for="email" class="block text-sm font-medium text-gray-700">Email address</label>
        <input type="email" name="email" id="email" required class="mt-1 block w-full rounded-md border-gray-300 shadow-sm focus:border-indigo-500 focus:ring-indigo-500 sm:text-sm">
    </div>
    <div>
        <label for="password" class="block text-sm font-medium text-gray-700">Password</label>
        <input type="password" name="password" id="password" required class="mt-1 block w-full rounded-md border-gray-300 shadow-sm focus:border-indigo-500 focus:ring-indigo-500 sm:text-sm">
    </div>
    <div class="flex items-center justify-between">
        <div class="flex items-center">
            <input id="remember_me" name="remember_me" type="checkbox" class="h-4 w-4 text-indigo-600 border-gray-300 rounded focus:ring-indigo-500">
            <label for="remember_me" class="ml-2 block text-sm text-gray-900">Remember me</label>
        </div>
        <div class="text-sm">
            <a href="#" class="font-medium text-indigo-600 hover:text-indigo-500">Forgot your password?</a>
        </div>
    </div>
    <div>
        <button type="submit" class="px-4 py-2 bg-blue-500 text-white rounded-md">Sign in</button>
    </div>
</x-slate::form>
@endverbatim
</x-code-preview>

## Customization

The `Form` component is highly customizable, allowing you to control its appearance and behavior to fit the needs of your application. You can add additional attributes like `action`, `method`, `class`, and more to the form element itself, ensuring that it integrates seamlessly with your application's backend and front-end needs.