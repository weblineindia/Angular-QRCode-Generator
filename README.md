# AngularJS - QRCode Generator

`angular-weblineindia-qrcode-generator` is a fast and easy-to-use Ionic 3 and AngularJS 9.0 based QR Code component / module library to generate QR Codes in your Ionic and Angular 9 app with support for AOT and the Ivy compiler and runtime.

## Table of Contents

- [Demo App](#demo-app)
- [Install angular-weblineindia-qrcode 1.0.x with Angular 9](#install-angular-weblineindia-qrcode-10x-with-angular-9)
- [Features](#features)
- [Basic Usage](#basic-usage)
- [Examples: How to implement angular-weblineindia-qrcode](#examples-how-to-implement-angular-weblineindia-qrcode)
- [Generate a QR Code from a string - directive only](#generate-a-qr-code-from-a-string-directive-only)
- [Create a QR Code from a variable in your controller](#create-a-qr-code-from-a-variable-in-your-controller)
- [Parameters](#parameters)
- [Note](#note)
- [Available commands](#available-commands)
- [Want to Contribute?](#want-to-contribute)
- [Collection of Components](#collection-of-components)
- [Changelog](#changelog)
- [Credits](#credits)
- [License](#license)
- [Keywords](#keywords)


## Demo App

[![](qrcode.gif)](https://github.com/weblineindia/Vue-URL-Component/qrcode.gif)

## Install angular-weblineindia-qrcode 1.0.x with Angular 9

```
# Angular 9 and Ionic
npm install angular-weblineindia-qrcode --save
# Or use yarn
yarn add angular-weblineindia-qrcode
```

## Features

- Ivy Compiler and Runtime Support
- angular-weblineindia-qrcode-generator is based on node-qrcode and ships a couple of new features (keeping all the known features)
- Append a CSS class with `cssClass`
- New `elementType` field: `url`, `img`, `canvas` and `svg`
- New `margin` field. Define how wide the quiet zone should be.
- New `scale`, scale factor. A value of 1 means 1px per module (black dot).
- New `version` field. QR Code version. If not specified the most suitable value will be calculated.

## Basic Usage

### Import the module and add it to your imports section in your main AppModule:

```
// File: app.module.ts
// all your imports
import { QRCodeModule } from 'angular-weblineindia-qrcode';

@NgModule({
declarations: [
  AppComponent
],
imports: [
  QRCodeModule
],
providers: [],
bootstrap: [AppComponent]
})
export class AppModule { }
```

## Examples: How to implement angular-weblineindia-qrcode

### Generate a QR Code from a string (directive only)

Now that Angular/Ionic knows about the new QR Code module, let's invoke it from our template with a directive. If we use a simple text-string, we need no additional code in our controller.

```
<qrcode [qrdata]="'Your data string'" [width]="256" [errorCorrectionLevel]="'M'"></qrcode>
```

### Create a QR Code from a variable in your controller

In addition to our `<qrcode>`-directive in `example.html`, lets add two lines of code to our controller `example.ts`.

```
// File: example.ts
export class QRCodeComponent {
  public myAngularxQrCode: string = null;
  constructor () {
    // assign a value
    this.myAngularxQrCode = 'Your QR code data string';
  }
}

// File: example.html
<qrcode [qrdata]="myAngularxQrCode" [width]="256" [errorCorrectionLevel]="'M'"></qrcode>
```

## Parameters

| Attribute            | Type    | Default     | Description                                                    |
| -------------------- | ------- | ----------- | -------------------------------------------------------------- |
| allowEmptyString     | Boolean | false       | Allow empty string                                             |
| colorDark            | String  | '#000000ff' | RGBA color, color of dark module                               |
| colorLight           | String  | '#ffffffff' | RGBA color, color of light module                              |
| cssClass             | String  | 'qrcode'    | CSS Class                                                      |
| elementType          | String  | 'canvas'    | 'canvas', 'svg', 'img', 'url' (alias for 'img')                |
| errorCorrectionLevel | String  | 'M'         | QR Correction level ('L', 'M', 'Q', 'H')                       |
| margin               | Number  | 4           | Define how much wide the quiet zone should be.                 |
| qrdata               | String  | ''          | String to encode                                               |
| scale                | Number  | 4           | Scale factor. A value of 1 means 1px per modules (black dots). |
| version              | Number  | (auto)      | 1-40                                                           |
| width                | Number  | 10          | Height/Width (any value)                                       |

## Note

Depending on the amount of data of the _qrdata_ to encode, a minimum _width_ is required.



## Available commands

    # Build
    npm run build

## Want to Contribute?

- Created something awesome, made this code better, added some functionality, or whatever (this is the hardest part).
- [Fork it](http://help.github.com/forking/).
- Create new branch to contribute your changes.
- Commit all your changes to your branch.
- Submit a [pull request](http://help.github.com/pull-requests/).

---

## Collection of Components
 We have built many other components and free resources for software development in various programming languages. Kindly click here to view our [Free Resources for Software Development.](https://www.weblineindia.com/software-development-resources.html)
 
---

## Changelog

Detailed changes for each release are documented in [CHANGELOG.md](./CHANGELOG.md).

## Credits

angular-weblineindia-qrcode-generator is inspired by the [angularx-qrcode](https://www.npmjs.com/package/angularx-qrcode).

## License

[MIT](LICENSE)

[mit]: https://github.com/weblineindia/Vue-QRCode/blob/master/LICENSE

## Keywords

angular-weblineindia-qrcode-generator, angular-qrcode, ng-qrcode, ngx-qrcode, angular9, ionic, ionic3, ionic4, aot, aot-compatible, aot-compilation, library, ng, typescript
