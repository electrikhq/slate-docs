---
title: "Cards"
description: "Learn how to use the Card component in Electrik Slate UI"
---

# Cards

The `Card` component in Electrik Slate UI is a versatile and customizable container element that allows users to group and display content in a structured way. It supports various features like dark mode, customizable sizes, headers, footers, icons, and outlined styles.

## Props

| Prop Name  | Type    | Default  | Description                                                                                              |
|------------|---------|----------|----------------------------------------------------------------------------------------------------------|
| `size`     | String  | `md`     | The size of the card (`sm`, `md`, `lg`).                                                                  |
| `color`    | String  | `white`  | The background color of the card (`black`, `white`, or any other Tailwind color).                         |
| `outlined` | Boolean | `false`  | Whether the card should have an outlined style.                                                           |
| `header`   | String  | `null`   | Optional header content for the card.                                                                     |
| `footer`   | String  | `null`   | Optional footer content for the card.                                                                     |
| `icon`     | String  | `null`   | An optional icon to display in the header.                                                                |

## Examples

### Basic Usage

The following example demonstrates a simple card with a white background and default size:

<x-code-preview>
@verbatim
<x-slate::card>
    This is a basic card with default settings.
</x-slate::card>
@endverbatim
</x-code-preview>

### Card with Header and Footer

This example shows how to use a card with a header and footer:

<x-code-preview>
@verbatim
<x-slate::card header="Card Header" footer="Card Footer">
    This is a card with a header and footer.
</x-slate::card>
@endverbatim
</x-code-preview>

### Outlined Card

This example shows a card with an outlined style:

<x-code-preview>
@verbatim
<x-slate::card color="primary" outlined>
    This is an outlined card.
</x-slate::card>
@endverbatim
</x-code-preview>

### Card with Icon in Header

This example shows a card with an icon in the header:

<x-code-preview>
@verbatim
<x-slate::card header="Notifications" icon="carbon-notification" outlined>
    You have 3 new notifications.
</x-slate::card>
@endverbatim
</x-code-preview>

### Cards with Black and White Modes

This example showcases cards using explicit black and white modes, which adapt correctly to dark mode:

<x-code-preview>
@verbatim
<x-slate::card color="black" size="lg">
    This is a black card.
</x-slate::card>
<x-slate::card color="white" size="lg" outlined class="mt-4">
    This is an outlined white card.
</x-slate::card>
@endverbatim
</x-code-preview>

### Customizing Card Size

You can control the size of the card using the `size` prop:

<x-code-preview>
@verbatim
<x-slate::card size="sm">
    Small card content.
</x-slate::card>
<x-slate::card size="lg" class="mt-4">
    Large card content.
</x-slate::card>
@endverbatim
</x-code-preview>

## Customization

The `Card` component is highly customizable, allowing you to control its appearance and behavior to fit the needs of your application. Whether you need a simple container, a card with a structured layout, or an outlined card for emphasis, the `Card` component can accommodate your design requirements.
