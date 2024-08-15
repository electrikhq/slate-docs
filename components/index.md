# Button Component Documentation

Welcome to the documentation for the Button component. This document will guide you through the usage of the Slate UI kit's button components.

## Basic Button

To use a basic button, simply insert the following Blade component where you need it:

```blade
<x-slate::button>
    Click me
</x-slate::button>
```

### Preview

[preview]
<x-slate::button
Click me
</x-slate::button>
[/preview]

Primary Button
For a primary button, add the type attribute and set it to primary:

```blade
<x-slate::button type="primary">
    Primary Action
</x-slate::button>
```

### Preview

[preview]
<x-slate::button type="primary">
Primary Action
</x-slate::button>
[/preview]

Disabled Button
To disable a button, add the disabled boolean attribute:

```blade
<x-slate::button disabled>
    I'm Disabled
</x-slate::button>
```

### Preview

[preview]
<x-slate::button disabled>
I'm Disabled
</x-slate::button>
[/preview]
