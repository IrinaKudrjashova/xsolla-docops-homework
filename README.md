# Xsolla Login Widget Integration
## Introduction
This SDK integrates Xsolla Login Widget with a website. It supports two types of authorization:
* via login/password;
* via social networks.
## Implementation

### Step 1
Connect Xsolla Login Javascript SDK:
* If your project uses [Bower](http://bower.io/), launch the console and run the following command:

`bower install xsolla-login-js-sdk`

* If you don’t have the package installed, add the following code to the `<head>` tag of  
the web page where you want to place the widget:

```
<script
src="https://cdn.xsolla.net/xsolla-login-widget/sdk/2.1.1/xl.min.js"></scri
pt>
```

### Step 2
Add the widget initialization code to the `<body>` tag.

```
<script type="text/javascript">  
  XL.init({  
  projectId: '{Login ID}',  
  callbackUrl: '{callbackUrl}'  
});  
</script>
```

| Parameter  | Description                                                                                                                                                                     |
|---------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `projectId`   | Login ID from Publisher Account required                                                                                                                                           |
| `callbackUrl` | URL to redirect the user to after authentication. Must be identical to Callback URL specified in Publisher Account in Login settings. Required if there are several Callback URLs. |

### Step 3
Choose the way of placing the widget on the website:
* fullscreen mode;
* block of the page.

For the fullscreen mode add the button with an on-click event to your website and  
call the `XL.show()` function.

`<button onclick="XL.show()">Fullscreen widget</button>`

The fullscreen mode will be closed upon clicking outside the widget.

For the block of the page add the block, in which the widget will be placed, to the  
`<body>` tag of this page and specify the block ID.

`<div id="xl_auth"></div>`

Add the following script and specify the parameters as described below.

```
<script type="text/javascript">
var options = {
  width: 400,
  height: 550
};
XL.AuthWidget(element_id, options);
</script>
```

| Parameter | Description                                                                  |
|-----------|------------------------------------------------------------------------------|
| `options` | Login Widget block settings. The object consists of parameters listed below. |
| `width`   | Block width in pixels. Default is 400.                                       |
| `height`  | Block height in pixels. Default is 550.                                      |

## FAQ

| Questions                                                                    | Answers                                                                       |
|------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| I can't find Login ID                                                        | Go to your Publisher Account > Login settings  > General settings > Login ID  |
| Where I can find the guide describing the full integration  of Xsolla Login? | http://developers.xsolla.com/doc/login                                        |

