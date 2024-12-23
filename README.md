# Splash Colors in One CSS File

This project was inspired by [todepond](https://todepond.com/).

The idea is to map RGB color values from 0 to 9, instead of the usual 0 to 255. This makes it much easier to manage and choose colors.
If you haven't already, go read the blog post for more context and inspiration: [todepond blog](https://www.todepond.com/lab/splash/).

```scss
@function splash($r, $g, $b) {
    // 255/9 ≈ 28.34
    @return rgb($r * 28.34, $g * 28.34, $b * 28.34);
  }
```
