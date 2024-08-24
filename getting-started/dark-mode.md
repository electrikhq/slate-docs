---
title: "Dark Mode Support"
description: "Learn how to use and customize dark mode in Electrik Slate"
sidebar_order: 4
---

# Dark Mode Support

Electrik Slate comes with built-in support for dark mode, allowing your application to seamlessly switch between light and dark themes based on user preferences or system settings. This ensures that your UI remains consistent and visually appealing across different environments.

## Enabling and Customizing Dark Mode

### How It Works

Dark mode support in Electrik Slate is managed by Tailwind CSS. By default, Electrik Slate automatically detects the user's system preferences and applies the appropriate theme. This is achieved through Tailwind's `dark` variant, which allows you to apply styles conditionally based on the user's dark mode settings.

### Example: Dark Mode in Action

<x-code-preview>
@verbatim
<div class="bg-white dark:bg-black p-4 rounded-md shadow-lg">
    <h2 class="text-gray-900 dark:text-white">Dark Mode Example</h2>
    <p class="text-gray-700 dark:text-gray-300">
        This component automatically adapts to dark mode based on user preferences.
    </p>
</div>
@endverbatim
</x-code-preview>


In the example above, the `bg-white` and `text-gray-900` classes apply in light mode, while `dark:bg-black` and `dark:text-white` classes apply in dark mode. The component seamlessly transitions between these themes based on the user's system settings.

## Disabling or Customizing Dark Mode

If you prefer to disable dark mode or customize how it's implemented, you can do so in your `tailwind.config.js` file.

### Disabling Dark Mode

To disable dark mode, simply remove or comment out the `darkMode` configuration in your `tailwind.config.js` file:

```javascript
// tailwind.config.js
module.exports = {
    // darkMode: 'class', // Remove or comment this line to disable dark mode
    theme: {
        extend: {
            // Your customizations here
        },
    },
    plugins: [],
};
```

### Forcing Dark Mode in Previews

Sometimes, you might want to force a component to render in dark mode, regardless of the user's system settings. You can do this by adding the `dark` class to a wrapper element around your component:

<x-code-preview>
@verbatim

<div class="dark">
    <div class="bg-white dark:bg-black p-4 rounded-md shadow-lg">
        <h2 class="text-gray-900 dark:text-white">Forced Dark Mode Example</h2>
        <p class="text-gray-700 dark:text-gray-300">
            This component is forced to render in dark mode, regardless of system settings.
        </p>
    </div>
</div>
@endverbatim
</x-code-preview>


In this example, the `dark` class is applied to the outer `div`, forcing all nested elements to render in dark mode. This is useful for component previews in documentation or when you want to showcase how a component looks in dark mode.

## Customizing Dark Mode Colors

You can customize the colors used in dark mode by extending the Tailwind CSS theme in your `tailwind.config.js` file:

```javascript
// tailwind.config.js
module.exports = {
    darkMode: 'class', // Keep this enabled to use dark mode
    theme: {
        extend: {
            colors: {
                // Customize dark mode colors here
                black: '#111',
                white: '#f9f9f9',
                gray: {
                    900: '#1a1a1a',
                    800: '#2e2e2e',
                    700: '#4a4a4a',
                },
                // Add more colors as needed
            },
        },
    },
    plugins: [],
};
```

In this example, you can see how the colors used in dark mode can be customized. This allows you to tweak the appearance of your UI to better match your brand or design preferences.

### Example: Custom Dark Mode Colors

<x-code-preview>
@verbatim

<div class="bg-white dark:bg-gray-900 p-4 rounded-md shadow-lg">
    <h2 class="text-gray-900 dark:text-gray-200">Custom Dark Mode Colors</h2>
    <p class="text-gray-700 dark:text-gray-400">
        This component uses customized colors for dark mode, defined in the Tailwind config.
    </p>
</div>
@endverbatim
</x-code-preview>


This example shows how you can use your customized dark mode colors within components.

### Example: Custom Dark Mode Colors with Slate Components

<x-code-preview>
@verbatim
<div class="p-4 bg-gray-50 dark:bg-gray-900 rounded-lg shadow-lg">
    <h2 class="text-gray-900 dark:text-gray-200">Custom Dark Mode Colors</h2>
    <x-slate::badge color="primary">Primary Badge</x-slate::badge>
    <x-slate::badge color="secondary" class="ml-4">Secondary Badge</x-slate::badge>
</div>
@endverbatim
</x-code-preview>

In this example:

The background color is customized for both light and dark modes using custom colors defined in the tailwind.config.js file.
The Slate::badge components adapt to these custom colors, showing how flexible dark mode customization can be.