---
title: OnClientItemBlur
page_title: OnClientItemBlur | UI for ASP.NET AJAX Documentation
description: OnClientItemBlur
slug: menu/client-side-programming/events/onclientitemblur
tags: onclientitemblur
published: True
position: 12
---

# OnClientItemBlur





## 

The __OnClientItemBlur__ client-side event occurs when an item in the menu loses focus.

The event handler receives two parameters:

1. The instance of the menu firing the event.

1. An eventArgs parameter containing the following method:

* __get_item__ returns a reference to the __RadMenuItem__ that lost focus.

* __get_domEvent__ returns a reference to the DOM event that caused the blur.

You can use this event to respond when an item loses focus.

````ASPNET
	    <script type="text/javascript">
	        function BlurItem(menu, args) {
	            alert("Leaving " + args.get_item().get_text());
	        }
	    </script>
	
	    <telerik:RadMenu ID="RadMenu1" runat="server" Flow="Horizontal" OnClientItemBlur="BlurItem">
	        <Items>
	            ...
	        </Items>
	    </telerik:RadMenu>
````



# See Also

 * [OnClientItemFocus]({%slug menu/client-side-programming/events/onclientitemfocus%})

 * [OnClientMouseOut]({%slug menu/client-side-programming/events/onclientmouseout%})

 * [Overview]({%slug menu/client-side-programming/overview%})

 * [RadMenuItem Object]({%slug menu/client-side-programming/objects/radmenuitem-object%})