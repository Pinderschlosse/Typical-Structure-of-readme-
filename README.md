# XSOLLA Login Widget SDK

This SDK allows you to quickly integrate Xsolla Login Widget with your website.

Currently SDK supports following types of authorization:

+ via login/password
+ via social networks

More methods on its way.


## Getting started


### *Requirements*

+ [Xsolla Login Javascript SDK](https://github.com/xsolla/xsolla-login-js-sdk)
+ Windows 7,8 or MacOS

### *Installation*

<pre style="background-color: #a8dbff"><strong>Notice:</strong> If you already have installed Xsolla Login Javascript SDK, please go to section <strong>Usage</strong></pre>

Connect Xsolla Login Javascript SDK:

- If your project uses [Bower](http://bower.io/), launch the console and run the following command:

<l style="background-color: #000000; color: #ffffff">bower install xsolla-login-js-sdk</l>

- If you don’t have the package installed, add the following code to the `<head>` tag of the web page where you want to place the widget:

```html
<script src="https://cdn.xsolla.net/xsolla-login-widget/sdk/2.1.1/xl.min.js"></script>
```


## Usage


### Step 1


Add the widget initialization code to the `<body>` tag.

```javascript
<script type="text/javascript">
XL.init({
  projectId: '{Login ID}',
  callbackUrl: '{callbackUrl}'
});
</script>
```

**Parameter**|**Description**
:------:|:------
`projectId`|Login ID from Publisher Account. Required.
`callbackUrl`|URL to redirect the user to after authentication. Must be identical to Callback URLspecified in Publisher Account in Login settings. Required if there are several Callback URLs.

### Step 2

Select the way of placing the widget on the website:

+ fullscreen mode
+ particular block of the page

***FULLSCREEN MODE***

Add the button with an on-click event to your website and call the `XL.show()` function.

```html
<button onclick="XL.show()">Fullscreen widget</button>
```

The fullscreen mode will be closed upon clicking outside the widget.


***BLOCK OF THE PAGE***

Add the block, in which the widget will be placed, to the `<body>` tag of this page and specify the block ID.

```html
<div id="xl_auth"></div>
```

Add the following script and specify the parameters as described below.

```javascript
<script type="text/javascript">
var options = {
  width: 400,
  height: 550
};
XL.AuthWidget(element_id, options);
</script>
```

**Parameter**|**Description**
:------:|:------
`options`|Login Widget block settings. The object consists of the parameters listed below.
`width`|Block width in pixels. Default is 400.
`height`|Block height in pixels. Default is 550.

## Troubleshooting

1. **I can’t find Login ID. Where is it?**

    *Answer*: Please go to your Publisher Account > Login settings > General settings > Login ID.
2. **Where can I find the guide described full integration of Xsolla Login?**

    *Answer*: Please follow the [link](http://developers.xsolla.com/doc/login).
