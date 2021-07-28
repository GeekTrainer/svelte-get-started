With your application scaffolded, let's explore two key files, *App.svelte* and *main.js*, which serve as the entry point.

## App.svelte

Traditionally, the core component for Svelte applications is App.svelte. The template provides a relatively small component, which allows a developer to quickly modify it (or recreate it) as needed.

```html
<script>
    export let name;
</script>

<main>
    <h1>Hello {name}!</h1>
    <p>Visit the <a href="https://svelte.dev/tutorial">Svelte tutorial</a> to learn how to build Svelte apps.</p>
</main>

<style>
    /* snipped style */
</style>
```

### script

Notice the `script` tag. A single variable `name` is declared with the keyword `export`. By declaring a variable in Svelte it is automatically reactive, meaning you can display the value using the handlebars syntax (`{ }`), and your page will automatically update if the value is modified.

The `export` marks `name` as a property or prop. Props allow for a component to accept values from a parent, much in the same way HTML tags like `a` and `img` have attributes. Props will be explored further in a separate module.

### HTML

In the middle of *App.svelte* you will see the HTML contained inside `main`. `main` is an HTML5 tag used to indicate the central content area. `main` is **not** required, and is simply included as a good convention. You are free to use whatever HTML you wish in a component, as long as all tags are closed correctly.

`<h1>Hello {name}!</h1>` is used to display the value of `name`. The handlebar syntax (`{ }`) can be used for both HTML and attribute values.

### style

The template provides a generic style for the page. You are free to modify the style, or import a framework such as Bootstrap or Tailwind.

## main.js

*main.js* mounts *App.svelte*.

```javascript
import App from './App.svelte';

const app = new App({
    target: document.body,
    props: {
        name: 'world'
    }
});

export default app;
```

It starts by using `import` to load the component in *App.svelte*, much in the same way you import another package. While there is no requirement to name the imported value the same as the file, it's a good practice to use the same name as it makes your project more readable.

After importing, a new object is created using the imported component. `target` is used to indicate where on the page you wish to display the component; `document.body` is typically used to replace the viewport of the page with the component. Finally, `name` is passed in using `props` as `name` was declared in the component using `export`.

Lastly, the newly created object is exported. *main.js* is imported from *index.html* in the template, so the component is displayed on the page.
