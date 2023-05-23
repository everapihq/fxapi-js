<p align="center">
<img src="https://app.fxapi.com/img/logo/fxapi.png" width="300"/>
</p>

# fxapi-js: JS Currency Converter
Fxapi.com is a foreign exchange rates API that provides historic & realtime data.
This package is a JavaScript wrapper for [fxapi.com](https://fxapi.com) that aims to make the usage of the API as easy as possible in your project.

## Installation

### npm
```shell
npm install --save @everapi/fxapi-js
```
### yarn
```shell
yarn add @everapi/fxapi-js
```

## Import

```js
import FxAPI from '@everapi/fxapi-js';
```

or use it directly in a Browser:

```html
<script src="path/to/fxapi-js/index.js"></script>
```

## Usage

Initialize the API with your API Key (get one for free at [fxapi.com](https://fxapi.com)):

```js
const fxApi = new FxAPI('YOUR-API-KEY');
```

Afterwards you can make calls to the API like this:

```js
fxApi.latest({
        base_currency: 'USD',
        currencies: 'EUR'
    }).then(response => {
        console.log(response);
    });
```

Endpoints accessible with a free account:
- `status`
- `currencies`
- `latest`
- `historical`

These advanced endpoints currently require a paid subscription:
- `convert`
- `range`

Find out more about our endpoints, parameters and response data structure in the [docs](https://fxapi.com/docs)

## License

The MIT License (MIT). Please see [License File](LICENSE.md) for more information.

[docs]: https://fxapi.com/docs
[fxapi.com]: https://fxapi.com
