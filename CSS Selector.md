##### Tag name = div

```css
div
```

##### Tag name = div & class = result

```css
div.result
```

##### Id = name

```css
#name
```

##### Select   'div.result' if they are dependent (related indirectly) of 'div.cw'

```css
div.cw div.result
```

##### Select only 'div.result' if they are dependent (related directly) of 'div.cw'

```css
div.cw > div.result
```

##### Select `ol` or `ul` tags that are dependent to the `ol,ul`

```css
ol > li, ul > li
```

##### Select `style` attribute

```css
[style]
```

##### Select `a` tags with `style` attribute that is equal to `images`

```css
a[style='images']
```

##### Select `div` with `class` attribute that contain `images`

```css
div[class*='images']
```

##### Select `div` with `result` class that not contain `result--more` class

```css
div.result:not(.result--more)
```

##### Select `div` tag with `result` class that is `5s` child of the data

```css
div.result:nth-child(5)
```

##### Complex query

```css
div > a[role="menuitem"][tabindex]#option-2--menu--1
```