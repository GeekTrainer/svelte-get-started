Svelte is a frontend JavaScript framework for creating reactive full-stack web applications. Unlike many other frameworks, Svelte requires the use of a particular file type (a *svelte* file), and handles the conversion to HTML, CSS and JavaScript at compile time. Svelte provides a development experience which can feel very natural to JavaScript developers while offering increased performance.

## The Svelte component

The Svelte file, or component, is the heart of any Svelte application. Components have three main sections - `style` for any CSS, `script` for any JavaScript, and the HTML you wish to display to the user.

```html
<script>
    // JavaScript goes here
</script>

<!-- HTML goes here -->

<style>
    /* CSS goes here */
</style>
```

> [!NOTE] Svelte [natively supports TypeScript](https://svelte.dev/blog/svelte-and-typescript). If you wish to use TypeScript for your Svelte projects, you will perform [one additional setup step](https://svelte.dev/blog/svelte-and-typescript#Adding_TypeScript_to_an_existing_project), and use the `lang="ts"` on the `script` tag.

Components use a *svelte* extension. A build process is required to convert the contents of the files to the associated HTML, CSS and JavaScript for the browser to run. As we will see, scaffolding is available with a build process preconfigured.
