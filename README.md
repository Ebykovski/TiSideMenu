TiSideMenu
===========================================

** iOS 7 ONLY **

iOS 7 style side menu with parallax effect.

Wrapper module for the great [RESideMenu](https://github.com/romaonthego/RESideMenu)

<img src="https://github.com/mpociot/TiSideMenu/raw/master/Demo.gif" alt="RESideMenu Screenshot" width="320" height="568" />

Usage
====================

Use TiSideMenu as a replacement for your root window.

	var contentView = Ti.UI.createWindow({
		background: 'red'
	});
	
	var menuView    = Ti.UI.createWindow({
		background: 'transparent'
	});
	
	var win = TiSideMenu.createSideMenu({
		contentView: 		contentView,
		menuView: 			menuView,
		backgroundImage: 	'stars.png',
		contentViewScaleValue: 0.2, 		// Default 0.5
		scaleContentView: true,				// Default: true
		panGestureEnabled: false,			// Default: true
		scaleBackgroundImageView: false,	// Default: true
		parallaxEnabled: false				// Default: true
	});
	win.open();

Configuration
===
	
* Enable / Disable the pan gesture 
	`win.setPanGestureEnabled( true / false );`
	
* Enable / Disable Parallax effect	
	`win.setParallaxEnabled( true / false ); `
	
* Enable / Disable Background image scaling
	`win.setScaleBackgroundImageView( true / false );`
	
* Enable / Disable Content view scaling
	`win.setScaleContentView( true / false );`
	
* Set the content view scale value
	`win.setContentViewScaleValue( 0.0 - 1.0 );`

Manually showing / hiding the menu:

`win.hideMenuViewController()`

`win.presentMenuViewController()`

Events
===

	
	win.addEventListener("willShowMenuViewController",function()
	{
		alert("Will show menu view controller");
	});

	win.addEventListener("didShowMenuViewController",function()
	{
		alert("Did show menu view controller");
	});

	win.addEventListener("willHideMenuViewController",function()
	{
		alert("Will hide menu view controller");
	});

	win.addEventListener("didHideMenuViewController",function()
	{
		alert("Did hide menu view controller");
	});



ABOUT THE AUTHOR
========================
I'm a web enthusiast located in Germany.

Follow me on twitter: @marcelpociot