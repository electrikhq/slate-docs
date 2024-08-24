---
title: "Introduction"
description: "What is Slate?"
sidebar_order: 1
---

# Introduction
Electrik Slate UI Kit is a set of beautiful anonymous blade components built using [tailwindcss](https://tailwindcss.com) for your next [Laravel](https://laravel.com) project.

## Requirements

- PHP 7.4+
- Laravel 7+
- Tailwindcss
- Alpine.js (required for some components)

Slate UI kit is entirely dependent on Tailwind CSS. If you are using another CSS framework, conflicts may occur. It is not advised to use this kit with any other CSS framework.

## How does it look?
Below are some examples of the Slate components

### Buttons
Below are various button with different props

<x-code-preview>
@verbatim
<x-slate::button color="primary">
    Primary button
</x-slate::button>
<x-slate::button color="secondary">
    Secondary button
</x-slate::button>
<x-slate::button color="primary" disabled>
    Disabled button
</x-slate::button><br/><br/>
<x-slate::button icon="carbon-arrow-right" icon-position="after">
    Button with icon
</x-slate::button>
@endverbatim
</x-code-preview>

### Badges

Everything in Electrik Slate is driven by props. These props are same as how Blade props work.

<x-code-preview>
@verbatim
<x-slate::badge color="primary">
    primary
</x-slate::badge>
<x-slate::badge color="black" outlined size="sm">
    small outlined
</x-slate::badge>
<x-slate::badge color="black" size="lg">
    large
</x-slate::badge>
@endverbatim
</x-code-preview>
