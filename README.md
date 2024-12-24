# Splash Colors in One CSS File

This project was heavily inspired by [todepond](https://www.todepond.com/lab/splash/).

The idea is to map RGB color values from 0 to 9, instead of the usual 0 to 255. This makes it much easier to manage and choose colors.
If you haven't already, go read the blog post for more context and inspiration: [todepond blog](https://www.todepond.com/lab/splash/).

Here is a simple implementation in Scss:
```scss
@function splash($r, $g, $b) {
    // 255/9 ≈ 28.34
    @return rgb($r * 28.34, $g * 28.34, $b * 28.34);
  }
  // color: splash(5,5,5) -> gray
```

Unfortunately, normal CSS does not support this at all, not even the concept of custom color spaces. So, this repo provides an alternative way: `--spRGB`. For example, `--sp555` would be gray.

## Getting Started

There are two ways to use this repo:

1.  **Using the CSS file directly:**
    Include the compiled CSS file from github in your HTML:
    ```html
    <link rel="stylesheet" href="https://cdn.jsdelivr.net/gh/matan-h/splash-css@master/dist/styles.css">
    ```
    You can now use it in your CSS like `--sp555` for gray.
2.  **Compiling with pnpm:**
    -   Clone the repository.
    -   Run `pnpm install` to install the dependencies.
    -   Run `pnpm build` to compile the SCSS into CSS.
    -   Use the generated `dist/styles.css` file in your project.
