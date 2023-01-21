# vue-qrcode-component

Create QR codes with a simple Vue component, forked from <a chref="https://github.com/gerardreches/vue-qrcode-component">gerardreches/vue-qrcode-component</a> and updated for Vue 3 and Vite.

[Demo and Documentation on GitHub Pages](https://walokra.github.io/vue-qrcode-component/)

## Installation

Install the package:

```shell
npm install vue-qrcode-component
```

Then register the component:

```js
import { createApp } from 'vue'
import VueQRCodeComponent from 'vue-qrcode-component'

const app = createApp(App)
app.component('qr-code', VueQRCodeComponent)
```

Now you can use it as:

```html
<qr-code text="Text to encode"></qr-code>
```

## Usage

### Props

| prop        | type   | required | default | validation                         |
|-------------|--------|----------|---------|------------------------------------|
| text        | String | true     |         |                                    |
| size        | Number | false    | 256     |                                    |
| color       | String | false    | '#000'  |                                    |
| bg-color    | String | false    | '#FFF'  |                                    |
| error-level | String | false    | 'H'     | Only accepts 'L', 'M', 'Q' or 'H'. |

_**Note:** size prop uses pixels units._

### Example

We will generate a QR code that gives an URL on decode. It measures 500x500 px, uses a yellow color for the code and a blue color for the background. This QR will use a **Low** error correction level.

```html
<qr-code
    text="https://goo.gl/9eIWP9"
    size="500"
    color="#f1c40f"
    bg-color="#3498db"
    error-level="L">
</qr-code>
```
