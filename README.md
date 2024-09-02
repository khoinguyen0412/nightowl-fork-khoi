![image](https://github.com/bufferhead-code/nightowl/assets/6266887/6dbd652a-0307-4d2b-ac9e-26230b8b59c7)

> [!NOTE]
> Check out **solidtime - The modern Open Source Time-Tracker** at [solidtime.io](https://www.solidtime.io)

## Nightowl

A "micro-framework" (\*hacky script) that adds dark mode to any website with a single line of code. The script has been modified by me for my needs.

**You can learn more about how it works and how the owner made it [here](http://www.youtube.com/watch?v=JONzCyVXa60)**.

[![Youtube Video about how this project was made](http://img.youtube.com/vi/JONzCyVXa60/0.jpg)](http://www.youtube.com/watch?v=JONzCyVXa60 'Add Dark Mode to any Website with a single line of code')

## State of the Project
This is the modified version of the original repo to fit my projects. 

## Changes
I made some changes to the CSS selectors so that the filter won't be applied to the nav tag which is fixed for most of the website and the main content of the body will be apply with the dark mode filter.

```html
<body>
     <header>
        <nav></nav>
    </header>
    <div id="webPage">
    </div>
</body>
```


## Integration

Integration can be achieved by one of the following methods.

### npm

To use nightowl with a bundler like Vite first install it with this command:

```shell
npm i @khoinguyen0412/nightowl
```

Then add these lines to your HTML file:

```html
<script type="module">
    import { createNightowl } from '@khoinguyen0412/nightowl'

    createNightowl({
          defaultMode: 'dark',
          toggleButtonMode: 'newState',
          parentEle: 'navbar'
    })
</script>
```

## Configuration Options

### defaultMode

-   **Type:** `'light' | 'dark'`
-   **Default:** `'light'`

Sets the default mode for users that have not set a preference yet and do not have a system preference for dark mode.

### toggleButtonMode

-   **Type:** `'currentState' | 'newState'`
-   **Default:** `'currentState'`

### parentEle

-   **Type:** `'element's ID'`
-   **Default:** `''`

Configures what state of the toggle button should be shown to the user.

-   `currentState` - Shows the state that is currently applied to the website.
-   `newState` - Shows the state that will be applied when the user clicks the button.
-   `parentEle` - Optional choice where to append the toggle ( using parent element's id)

## Customize Dark Mode

You can exclude elements from being inverted in dark mode using the `.nightowl-daylight` CSS class. Just add it to an element and it will show the element in the same way as the light mode. 

```html
<div>
  <p>I'm inverted in Dark Mode</p>
  <p class="nightowl-daylight">I'm not inverted in Dark Mode</p>
</div>
```
## Credits

This project is heavily inspired by Aral Balkan who [wrote down this idea to implement dark mode in a few lines of CSS using CSS Filters](https://ar.al/2021/08/24/implementing-dark-mode-in-a-handful-of-lines-of-css-with-css-filters/).

This orginal repo is from [bufferhead-code](https://github.com/bufferhead-code)
