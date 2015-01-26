# jsprop
Visual Studio 2013 snippet that creates C# like properties for Javascript

I've encountered myself many times writing properties in Javascript of the like

 


	var _appIsSecure = {
		secured: false,
		get: function () {
			return this.secured;
		},
		set: function (value) {
			this.secured = value;
		}
	};

That kind of "property" allows me to define a namespace thaks to [WinJS.Namespace.define](https://msdn.microsoft.com/en-us/library/windows/apps/br212667.aspx) and use the following code:

	WinJs.Namespace.define("MyNamespace", {
		appSecured: _appIsSecure
	});

Then, anywhere in my code I can either set 

	MyNamespace.appSecured = true;

or ask for the value of that property

	var sec = MyNamespace.appSecured;

The [jsprop.snippet](jsprop.snippet) file adds an easy snippet of code to your Visual Studio 2013 solution, allowing you to just type "prop" + Tab and a simple template for a property will show up.

It turned out to be pretty useful to me so I decided to put on GitHub. I hope it helps you too.

