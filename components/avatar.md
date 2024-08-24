---
title: "Avatars"
description: "Learn how to use the Avatar component in Electrik Slate UI"
---

# Avatars

The `Avatar` component in Electrik Slate UI is a versatile and customizable element that allows users to display profile pictures, initials, or status indicators. It supports various features like dark mode, customizable sizes, rounded corners, and outlined styles.

## Props

| Prop Name   | Type    | Default  | Description                                                                                              |
|-------------|---------|----------|----------------------------------------------------------------------------------------------------------|
| `size`      | String  | `md`     | The size of the avatar (`sm`, `md`, `lg`, `xl`).                                                          |
| `src`       | String  | `null`   | The image source URL for the avatar.                                                                      |
| `alt`       | String  | `''`     | The alt text for the image.                                                                               |
| `initials`  | String  | `null`   | The initials to display if no image is provided.                                                          |
| `rounded`   | Boolean | `true`   | Whether the avatar should be fully rounded.                                                               |
| `status`    | String  | `null`   | The status indicator (e.g., `online`, `offline`, `busy`).                                                 |
| `color`     | String  | `gray`   | The background color for initials and status indicator (`black`, `white`, or any other Tailwind color).   |
| `outlined`  | Boolean | `false`  | Whether the avatar should have an outlined style.                                                         |

## Examples

### Basic Usage

The following example demonstrates a simple avatar with an image and default size:

<x-code-preview>
@verbatim
<x-slate::avatar src="https://picsum.photos/id/237/200/300" alt="User Profile" />
@endverbatim
</x-code-preview>

### Avatar with Initials

This example shows how to display initials inside an avatar when no image is provided:

<x-code-preview>
@verbatim
<x-slate::avatar initials="JD" color="primary" />
@endverbatim
</x-code-preview>

### Rounded and Outlined Avatar

You can create rounded and outlined avatars using the `rounded` and `outlined` props:

<x-code-preview>
@verbatim
<x-slate::avatar initials="JD" color="secondary" rounded outlined />
@endverbatim
</x-code-preview>

### Avatar with Status Indicator

This example shows how to add a status indicator to an avatar:

<x-code-preview>
@verbatim
<x-slate::avatar src="https://picsum.photos/id/237/200/300" alt="User Profile" status="online" />
@endverbatim
</x-code-preview>

### Avatars with Black and White Modes

This example showcases avatars using explicit black and white modes, which adapt correctly to dark mode:

<x-code-preview>
@verbatim
<x-slate::avatar initials="AB" color="black" size="lg" />
<x-slate::avatar initials="CD" color="white" size="lg" outlined />
@endverbatim
</x-code-preview>

### Customizing Avatar Size

You can control the size of the avatar using the `size` prop:

<x-code-preview>
@verbatim
<x-slate::avatar initials="SM" color="success" size="sm" />
<x-slate::avatar initials="MD" color="info" size="md" />
<x-slate::avatar initials="LG" color="warning" size="lg" />
<x-slate::avatar initials="XL" color="danger" size="xl" />
@endverbatim
</x-code-preview>

## Customization

The `Avatar` component is highly customizable, allowing you to control its appearance and behavior to fit the needs of your application. Whether you need a simple profile picture, a placeholder with initials, or a status indicator, the `Avatar` component can accommodate your design requirements.
