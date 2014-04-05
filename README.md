Purpose
--------------

I recenty needed to build the iMessage style pull-to-reveal timestamps feature for a personal project and decided to open source the category. :)


Supported OS & SDK Versions
-----------------------------

* Supported build target - iOS 6.0
* Earliest supported deployment target - iOS 6.0


ARC Compatibility
------------------

The category will work correctly ONLY with ARC enabled.


Installation
--------------

To install, either copy the category into your project or add it to your podfile.

pod 'SPXRevealableView'


Usage
-------

Using this component is almost completely drop in, just follow a few simple steps:

		1. #import "UITableView+SPXRevealAdditions.h"
		2. [self.tableView enableRevealableViewForDirection:SPXRevealableViewGestureDirectionLeft];
		3. cell.revealableView = timestampView;
		
You should call enable at a fairly early stage in your UITableView's lifecycle, ideally in `-viewDidLoad`

To gain the benefits of reusable cells, I recommended setting the revealableView in your `-awakeFromNib` cell method, but you could declare it directly in your `-cellForRowAtIndexPath` method as is shown in the included demo.

That's it! It will automatically handle inserting the view into the cells, you have a nice property on each cell to make it simple to update and all gesture handling is done automatically for you just by including the class.


Feel free to use in any way you see fit. Please try and reference me somewhere in your app if you use this in a production app and maybe even tell me about it via Twitter [@shaps](http://twitter.com/shaps) ;)