The component is the heart of any Svelte project. Components use a *svelte* extension, and have sections for scripts, style and HTML.

## Create dynamic values

When working with any frontend framework, a primary focus is on dynamic data. As values change you typically need your application to respond. This might be displaying the new value, modifying what's currently displayed to the user, updating state, or other actions.

Svelte allows you to work with dynamic data without the need to register values using stores or other special tooling. To declare a dynamic value, you declare a JavaScript variable the same way you would any other variable:

```html
<script>
let name = 'Christopher';
</script>
```

> ![NOTE] As your application grows, you may wish to create a centralized store for values shared across multiple components. Fortunately Svelte can grow with you and supports creating stores.

## Display dynamic values

Svelte uses the common "handlebar" (`{ }`) syntax to interact with JavaScript from your HTML. To display the value of a variable, you place the name of the variable inside the curly braces:

```html
<div class="header">{ name }</div>
```

## Adding style

To add style to a component, you add the appropriate CSS to the `style` element in the component. The style added to a component is scoped to that component only, making it self-contained. If you wish to make a style global, you can use the `:global` directive.

```html
<style>
.header {
    font-weight: bold;
    /* applies only to header class in this component */
}

:global(h2) {
    font-color: blue;
    /* applies to ALL h2 elements in the project */
}
</style>
