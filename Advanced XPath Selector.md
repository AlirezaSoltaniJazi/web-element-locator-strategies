##### Select `div` tags that have another `div` tags as a children that contains a `data-result=snippet` attribute that have `span` tags that contains `Software Test Engineer` text

```xpath
//div//div[contains(@data-result,'snippet')]//span[contains(.,'Software Test Engineer')]
//div//div[contains(@data-result,'snippet')]//span[contains(text(),'Software Test Engineer')]
```

##### Select `div` tags that have another `div` tags as a children that contains a `data-result=snippet` attribute that is in the 5 index

```xpath
(//div//div[contains(@data-result,'snippet')])[5]
```

##### Select `a` tags that have `img` attribute as a children

```xpath
//a[.//img]
```

##### Select `a` tags that contains `class=zcm__link` attribute that are after `a` tags with `data-zci-link=news`

```xpath
//a[contains(@class, 'zcm__link')][preceding::a[@data-zci-link='news']]
```

##### Select `a` tags that contains `class=zcm__link` attribute that are before `a` tags with `data-zci-link=news`

```xpath
//a[contains(@class, 'zcm__link')][following::a[@data-zci-link='news']]
```

##### preceding-sibling and following-sibling
```xpath
//a[contains(@class, 'zcm__link')][following::a[@data-zci-link='news']]
```