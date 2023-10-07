### Selenium WebDriver locators

For example, Selenium WebDriver supports three other kinds of locators.

Link text locators match “a” elements that equal the given text. They are equivalent to the XPath: `//a[.=_’value’_]`.

Partial link text locators work the same as link text locators, except that they check if the text contains instead of
equals the value. They are equivalent to the XPath: `//a[contains(., ‘_value_’)]`.

Tag locators return all elements that use a given tag. For example, return all “p” elements. This locator type is not
very useful because pages usually have multiple elements for each tag in different locations. It is essentially
superseded by CSS selectors.

Link text locators can be helpful, but I almost never use tag locators.

### Playwright locators

If you are using Playwright for automation, Playwright offers a set of built-in locators that are friendlier for
programming:

page.getByRole() can locate by explicit and implicit accessibility attributes.

```js
await expect(page.getByRole('heading', {name: 'Sign up'})).toBeVisible();
```

page.getByText() can locate by text content.

```js
await expect(page.getByText('Welcome, John')).toBeVisible();
```

page.getByLabel() can locate a form control by the associated label's text.

```js
await page.getByLabel('Password').fill('secret');
```

page.getByPlaceholder() can locate an input by placeholder.

```js
await page
    .getByPlaceholder("name@example.com")
    .fill("playwright@microsoft.com");
```

page.getByAltText() can locate an element, usually image, by its text alternative.

```js
await page.getByAltText('playwright logo').click();
```

page.getByTitle() can locate an element by its title attribute.

```js
await expect(page.getByTitle('Issues count')).toHaveText('25 issues');
```

page.getByTestId() can locate an element based on its data-testid attribute (other attributes can be configured).

```js
await page.getByTestId('directions').click();
```

### Cypress

```xpath
data-cy
```

```xpath
data-test-id
```

### Locator order

Here’s my order of preference

1. Test ID using a data- attribute
2. ID (if the ID is unique on the page)
3. Input name (if the name is unique on the page)
4. Class name
5. Text value
6. CSS selector
7. XPath without text or indexing
8. Link text or partial link text
9. XPath with text and/or indexing