# New Properties:
`object-position: center`


# My notes:
1.  add width and height attributes to img tag (without units) so that the browser can set the proportion of the images and then lazy load the image

```HTML
<img
          src="https://source.unsplash.com/tR6PdtuxF-M/1200x1800"
          alt="Photo by Claudie-Ann Tremblay-cantin"
          width="4000"
          height="6000"
          loading="lazy"
  />
  ```

```css
img{
img {
  width: 20rem;
  height: auto;
  display: block;
}

}
```
lazy: it will load once it enters the viewport
eager: will load right away


2. Using Object-fit: control the width and height from the container of the image:
```css
.container {
  width: 75vw;
  height: 60vh;
  border: 1rem solid pink;
}

.the-image {
  width: inherit;
  height: inherit;
  object-fit: cover;
}
```

3. rounder images and square: [video](https://www.linkedin.com/learning/css-images/create-a-square-or-other-proportion-image?autoSkip=true&resume=false)
```html
  <figure class="card">
        <div class="ratio-box">
          <img
            src="https://source.unsplash.com/2B4dYFgYAyQ/1200x1800"
            alt="Photo by David Clode"
            class="the-image"
            width="3965"
            height="2736"
            loading="lazy"
          />
        </div>
        <figcaption>
```

```css
.card {
  width: 40vw;
  border: 3px solid black;
  border-radius: 1rem;
  overflow: hidden;
}

.the-image {
  width: 100%;
  height: 100%;
  object-fit: cover;
  position: absolute;
  top: 0;
}

figcaption {
  padding: 1rem;
}

.ratio-box {
  width: 100%;
  height: 0;
  padding-top: calc(100% * (1200 / 992)); (100% for square)
  position: relative;
}

```
