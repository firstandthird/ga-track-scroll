<h1 align="center">Google Analytics Scroll</h1>

<p align="center">
  <a href="https://github.com/firstandthird/ga-track-scroll/actions">
    <img src="https://img.shields.io/github/workflow/status/firstandthird/ga-track-scroll/Test/main?label=Tests&style=for-the-badge" alt="Test Status"/>
  </a>
  <a href="https://github.com/firstandthird/ga-track-scroll/actions">
    <img src="https://img.shields.io/github/workflow/status/firstandthird/ga-track-scroll/Lint/main?label=Lint&style=for-the-badge" alt="Lint Status"/>
  </a>
  <img src="https://img.shields.io/npm/v/@firstandthird/ga-track-scroll?style=for-the-badge" alt="NPM" />
</p>

Auto-track scroll depth for Google Analytics.

## Installation

```sh
npm install ga-track-scroll
```

_or_

```sh
yarn add ga-track-scroll
```

## Usage
```js
import 'ga-track-scroll'
```

Once the user starts scrolling it will send events to Google Analytics:

  * `category`: scroll
  * `action`: `document.location.toString()`
  * `label`: "Scrolled X%" (25/50/75/100) (There's also a simple `Scrolled` event the first time the user scrolls)
  * `value`: X (25/50/75/100)

It does also fire a custom event on the DOM:

```javascript
document.addEventListener('user:scroll', event => {
  const { amount } = event.detail; // Can be 25/50/75/100
});
```
