# Email service

[![Auxilin.com — Production ready Node, React starter kit for building products at a warp speed](https://raw.githubusercontent.com/auxilincom/component-template/master/assets/cover-black.png)](https://github.com/auxilincom/auxilin)

[![All Contributors](https://img.shields.io/badge/all_contributors-1-orange.svg?style=flat-square)](#contributors)
[![npm version](https://badge.fury.io/js/%40auxilin%2Femail-service.svg)](https://badge.fury.io/js/%40auxilin%2Femail-service) 
[![license](https://img.shields.io/github/license/mashape/apistatus.svg?style=flat-square)](https://github.com/auxilincom/email-service/blob/master/LICENSE)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg?style=flat-square)](http://makeapullrequest.com)
[![Build Status](http://ci.auxilin.com/api/badges/auxilincom/email-service/status.svg)](http://ci.auxilin.com/auxilincom/email-sercice)
[![David Dependancy Status](https://david-dm.org/auxilincom/email-service.svg)](https://david-dm.org/auxilincom/email-service)


[![Watch on GitHub](https://img.shields.io/github/watchers/auxilincom/email-service.svg?style=social&label=Watch)](https://github.com/auxilincom/email-service/watchers)
[![Star on GitHub](https://img.shields.io/github/stars/auxilincom/email-service.svg?style=social&label=Stars)](https://github.com/auxilincom/email-service/stargazers)
[![Follow](https://img.shields.io/twitter/follow/auxilin.svg?style=social&label=Follow)](https://twitter.com/auxilin)
[![Tweet](https://img.shields.io/twitter/url/https/github.com/auxiliccom/email-service.svg?style=social)](https://twitter.com/intent/tweet?text=I%27m%20using%20Auxilin%20components%20to%20build%20my%20next%20product%20🚀.%20Check%20it%20out:%20https://github.com/auxiliccom/email-service)
[![@auxilin](https://img.shields.io/badge/%F0%9F%92%AC%20Telegram-t.me/auxilin-blue.svg)](https://t.me/auxilin)

Email service is using [mailgun node client](https://www.npmjs.com/package/mailgun-js) to send emails.
We are inspired by [mjml](https://github.com/mjmlio/mjml) project. So, you can use mjml in your project and
after compiling templates to simple html files use our project to inject params by handlebars and send emails.
Let's dive into the docs.

## Installation

```bash
npm i @auxilin/email-service
```

## Quick example

To create a MailService class you should provide several params to its constructor
```javascript
const MailService = require('@auxilin/email-service');

const mailService = new MailService({
  isSendEmail: false, // you can prevent email sending by this param
  savedEmailHtmlPath: __dirname, // if you want to save your email as html in development mode
  mailgun: {  // configs for https://www.npmjs.com/package/mailgun-js
    apiKey: 'test',
    domain: 'test.info',
  },
  templatesDir: __dirname, // absolute path to templates directory
});
```

After that you are able to run **send** method with several params

```javascript
const result = await mailService.send(
  'email.html',
  { name: 'User name' },
  {
    from: 'Excited User <me@samples.mailgun.org>',
    to: 'test@test.com',
    subject: 'Test email',
  }
);
```

## Full API Reference

[API Reference](https://github.com/auxilincom/email-service/blob/master/API.md).

## Change Log

This project adheres to [Semantic Versioning](http://semver.org/).
Every release is documented on the Github [Releases](https://github.com/auxilincom/email-service/releases) page.

## License

Email-service is released under the [MIT License](https://github.com/auxilincom/email-service/blob/master/LICENSE).

## Contributing

Please read [CONTRIBUTING.md](https://github.com/auxilincom/email-service/blob/master/CONTRIBUTING.md) for details on our code of conduct, and the process for submitting pull requests to us.

## Contributors

Thanks goes to these wonderful people ([emoji key](https://github.com/kentcdodds/all-contributors#emoji-key)):

<!-- ALL-CONTRIBUTORS-LIST:START - Do not remove or modify this section -->
<!-- prettier-ignore -->
| [<img src="https://avatars2.githubusercontent.com/u/6461311?v=4" width="100px;"/><br /><sub><b>Evgeny Zhivitsa</b></sub>](https://github.com/ezhivitsa)<br />[💻](https://github.com/auxilin/email-service/commits?author=ezhivitsa "Code") [🤔](#ideas-ezhivitsa "Ideas, Planning, & Feedback") [📖](https://github.com/auxilin/email-service/commits?author=ezhivitsa "Documentation") |
| :---: |
<!-- ALL-CONTRIBUTORS-LIST:END -->

This project follows the [all-contributors](https://github.com/kentcdodds/all-contributors) specification. Contributions of any kind welcome!
