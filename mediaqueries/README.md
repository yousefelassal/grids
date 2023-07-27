## [Redefining Grid Areas with Media Queries](https://gridbyexample.com/examples/example13/)

```css
    .wrapper {
    display: grid;
    grid-gap: 1em;
    grid-template-areas:
     "header"
     "sidebar"
     "content"
     "sidebar2"
     "footer"
  }

  @media only screen and (min-width: 500px)  {
  .wrapper {

    grid-template-columns: 20% auto;
    grid-template-areas:
    "header   header"
    "sidebar  content"
    "sidebar2 sidebar2"
    "footer   footer";
  }
  }

  @media only screen and (min-width: 600px)   {
    .wrapper {
      grid-gap: 20px;
      grid-template-columns: 120px auto 120px;
      grid-template-areas:
      "header  header  header"
      "sidebar content sidebar2"
      "footer  footer  footer";
      max-width: 600px;
    }
  }
```