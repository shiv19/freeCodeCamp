---
id: 60fad6dfcc0d930a59becf12
title: Крок 38
challengeType: 0
dashedName: step-38
---

# --description--

HTML для реєстраційної форми завершено. Тепер ви можете його трохи прикрасити.

Почніть зі зміни шрифту на `Tahoma` та розміру шрифту на `16px` в `body`.

# --hints--

Ви повинні використати властивість `font-family`, щоб змінити шрифт.

```js
assert.isNotEmpty(new __helpers.CSSHelp(document).getStyle('body')?.fontFamily);
```

Ви повинні встановити властивість `font-family` на `Tahoma`.

```js
assert.equal(new __helpers.CSSHelp(document).getStyle('body')?.fontFamily, 'Tahoma');
```

Ви повинні встановити властивість `font-size` на `16px`.

```js
assert.equal(new __helpers.CSSHelp(document).getStyle('body')?.fontSize, '16px');
```

# --seed--

## --seed-contents--

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8">
    <title>Registration Form</title>
    <link rel="stylesheet" href="styles.css" />
  </head>
  <body>
    <h1>Registration Form</h1>
    <p>Please fill out this form with the required information</p>
    <form action='https://register-demo.freecodecamp.org'>
      <fieldset>
        <label>Enter Your First Name: <input type="text" name="first-name" required /></label>
        <label>Enter Your Last Name: <input type="text" name="last-name" required /></label>
        <label>Enter Your Email: <input type="email" name="email" required /></label>
        <label>Create a New Password: <input type="password" name="password" pattern="[a-z0-5]{8,}" required /></label>
      </fieldset>
      <fieldset>
        <label><input type="radio" name="account-type" /> Personal Account</label>
        <label><input type="radio" name="account-type" /> Business Account</label>
        <label>
          <input type="checkbox" name="terms" required /> I accept the <a href="https://www.freecodecamp.org/news/terms-of-service/">terms and conditions</a>
        </label>
      </fieldset>
      <fieldset>
        <label>Upload a profile picture: <input type="file" name="file" /></label>
        <label>Input your age (years): <input type="number" name="age" min="13" max="120" />
        </label>
        <label>How did you hear about us?
          <select name="referrer">
            <option value="">(select one)</option>
            <option value="1">freeCodeCamp News</option>
            <option value="2">freeCodeCamp YouTube Channel</option>
            <option value="3">freeCodeCamp Forum</option>
            <option value="4">Other</option>
          </select>
        </label>
        <label>Provide a bio:
          <textarea name="bio" rows="3" cols="30" placeholder="I like coding on the beach..."></textarea>
        </label>
      </fieldset>
      <input type="submit" value="Submit" />
    </form>
  </body>
</html>
```

```css
--fcc-editable-region--
body {
  width: 100%;
  height: 100vh;
  margin: 0;
  background-color: #1b1b32;
  color: #f5f6f7;

}
--fcc-editable-region--

label {
  display: block;
  margin: 0.5rem 0;
}

```
