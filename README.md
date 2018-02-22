jQuery Bootgrid Plugin [![Build Status](http://img.shields.io/travis/opnsense/jquery-bootgrid/master.svg?style=flat-square)](https://travis-ci.org/opnsense/jquery-bootgrid) ![Bower version](http://img.shields.io/bower/v/jquery.bootgrid.svg?style=flat-square) ![NuGet version](http://img.shields.io/nuget/v/jquery.bootgrid.svg?style=flat-square) ![NPM version](http://img.shields.io/npm/v/jquery-bootgrid.svg?style=flat-square) ![Gratipay](http://img.shields.io/gratipay/RafaelStaib.svg?style=flat-square)
============

Nice, sleek and intuitive. A grid control especially designed for bootstrap.

## Getting Started

**jQuery Bootgrid** is a UI component written for **jQuery** and **Bootstrap** (Bootstrap isn't necessarily required).

Everything you need to start quickly is:

1. Include **jQuery**, **jQuery Bootgrid** and **Bootstrap** libraries in your HTML code.
2. Define your table layout and your data columns by adding the `data-column-id` attribute.
3. Specify your data URL used to fill your data table and set ajax option to `true` directly on your table via data API.

```html
<!DOCTYPE html>
<html>
</html>
```

> For more information [check the documentation](http://www.jquery-bootgrid.com/Documentation).

### Examples

Examples you find [here](http://www.jquery-bootgrid.com/Examples).

## Reporting an Issue

Instructions will follow soon!

```html
<div data-action-links-id="myActionLinks">
  <a href="link_to_view/{id}">View {sender.email}</a>
  bootgridExecute[
    if('{sender.email}' == 'sender4@test.de') {
      '<a href="link_to_edit/{id}">Edit {sender.email}</a>'
    }
  ]end
</div>
```

Add a html formatter by adding the html-formatter option to your column like this:
```html
<th data-column-id="sender.email" data-html-formatter="myHtmlFormatter">Sender</th>
```
and this column will call a referenced div with the same html formatter. You can also execute javascript wrapped in <code>bootgridExecute[javascript code here]end</code> like this:
```html
<div data-html-formatter-id="myHtmlFormatter">
  <span class="label label-bootgridExecute['{sender.email}' == 'sender4@test.de' ? 'success' : 'warning']end">{sender.email}</span>
</div>
```

## Building

### Environment

jquery-bootgrid uses npm to install its own dependencies, and mono to build a NuGet package.

You should install both using your package manager. On macOS, this works as follows:
```
brew install npm
brew install mono
```

### Build dependencies

From the folder that jquery-bootgrid resides in, run:
```
npm install .
sudo npm install -g grunt
```

### Build jquery-bootgrid itself
```
grunt
```

If you are done with your modifications, you should increase the version number in boewer.json and package.json, 
update the changelog, and then run:
```
grunt release
```


## Contributing

No instructions yet.

## License

Copyright © 2014-2015 Rafael J. Staib
Copyright © 2018 Deciso B.V.

Licensed under the [MIT license](https://github.com/opnsense/jquery-bootgrid/blob/master/LICENSE.txt).
