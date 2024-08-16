---
title: "Installation"
description: "How to install and use Electrik Slate?"
sidebar_order: 3
---

# Installation

Start by installing the package using composer.

## Install package via composer

```bash
composer require electrik/slate
```

Many of Electrik Slate's component have (and will have) placeholders for icons. For these icons, it uses blade [blade-carbon-icons](https://github.com/codeat3/blade-carbon-icons). You may use other icon sets available here - [blade-icons](https://github.com/blade-ui-kit/blade-icons). Although officially we use only Carbon Icons.

## Install Tailwind CSS

If not already, install the npm dependencies for Tailwind CSS

```bash
npm install @tailwindcss/aspect-ratio @tailwindcss/forms @tailwindcss/typography --save-dev
```
You can find the detailed installation setup and steps for Tailwind CSS with Laravel [here](https://tailwindcss.com/docs/guides/laravel).

## Setup

In your Laravel's root tailwind.config.js file, require the plugins we installed as shown below:

```json
{
plugins: [
        require('@tailwindcss/aspect-ratio'),
        require('@tailwindcss/forms'),
        require('@tailwindcss/typography'),
    ],
...
}
```

Next, your should define the a color scheme for your project:

```json
{
...
theme: {
        extend: {
            colors: {
                danger: colors.rose,
                primary: colors.blue,
                success: colors.green,
                warning: colors.yellow,
            },
            fontFamily: {
                sans: ['Inter', ...fontFamily.sans],
            },
        },
    },
...
}
```
Your final tailwind.config.js should look like this:

```json
const colors = require('tailwindcss/colors')
const { fontFamily } = require('tailwindcss/defaultTheme')

module.exports = {
    purge: [
        './resources/**/*.blade.php',
        './vendor/electrik/slate/resources/views/components/**/*.blade.php',
    ],
    theme: {
        extend: {
            colors: {
                danger: colors.rose,
                primary: colors.blue,
                success: colors.green,
                warning: colors.yellow,
            },
            fontFamily: {
                sans: ['Inter', ...fontFamily.sans],
            },
        },
    },
    plugins: [
        require('@tailwindcss/aspect-ratio'),
        require('@tailwindcss/forms'),
        require('@tailwindcss/typography'),
    ],
}
```

## Start Using

That's it! Once installed and setup, you can start using the Slate UI Kit in your Laravel views.

For example, for badge using the following will generate badges

<x-code-preview>
@verbatim
<x-slate::badge color="success" size="xs">xs badge</x-slate::badge> <x-slate::badge color="info">default badge</x-slate::badge> 
@endverbatim
</x-code-preview>

Happy coding!
