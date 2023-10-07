##### Select `body` path that is direct children of `html` path

```xpath
/html/body
```

##### Select `input` tags

```xpath
//input
```

##### Select `a` tags that are direct children of the `p` tags

```xpath
//p/a
```

##### Select `any` children that are children of `div` tags

```xpath
//div//*
```

##### Select `role` attribute with value `list` that is inside of `ul` tags that are children of `div` tags

```xpath
//div//ul[@role='list']
```

##### Select `img` tags that have `height>120` and `width<220` attributes

```xpath
//img[@height>120][@width<220]
//img[@height>120 and @width<220]
```

##### Select `div` tags that have `input` tags that have attributes `name=va` or `name=t` or `id=searchbox_input`

```xpath
//div//input[@name='va' or @name='t' or @id='searchbox_input']
```

##### Select `div` tags have a `class` attribute that contains `xl:hidden` value

```xpath
//div[contains(@class,'xl:hidden')]
```

##### Select `div` tags have a `class` attribute that starts with `xl:hidden` value

```xpath
//div[starts-with(@class,'xl:hidden')]
```

##### Select `a` tags that `not contains` `target=_blank` attribute and have `target` attribute

```xpath
//a[not(contains(@target, '_blank'))][@target]
```