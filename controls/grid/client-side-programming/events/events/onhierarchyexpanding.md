---
title: OnHierarchyExpanding
page_title: OnHierarchyExpanding | UI for ASP.NET AJAX Documentation
description: OnHierarchyExpanding
slug: grid/client-side-programming/events/events/onhierarchyexpanding
tags: onhierarchyexpanding
published: True
position: 42
---

# OnHierarchyExpanding



## 

Telerik.Web.UI.GridDataItemCancelEventArgs OnHierarchyExpanding Property

>note To get or set property values for client API properties, you must call property accessor methods that are named with the get_ and set_ prefixes. For example, to get or set a value for a property such as[cancel](http://msdn.microsoft.com/en-us/library/bb310859.aspx), you call the get_cancel or set_cancel.
>


This event is fired when the hierarchy is being expanded and the HierarchyLoadMode setting is set to Client.


|  __Fired by__  | RadGrid |
| ------ | ------ |
| __Arguments__ | __id__ - id of the RadGrid item that has raised the event __itemIndexHierarchical__ - hierarchical index of the item that has raised the event __gridDataItem__ - the corresponding data item __tableView__ - owner TableView of the item that has raised the event __dataKeyValues__ - data key value for the item that has raised the event __domEvent__ - dom event that was raised for the current event|
| __Can be canceled__ |Yes, set eventArgs.set_cancel(true) to cancel|

Example:

````ASPNET
	    <telerik:RadGrid ID="RadGrid1" runat="server">
	        <ClientSettings>
	            <ClientEvents OnHierarchyExpanding="HierarchyExpanding" />
	        </ClientSettings>
	    </telerik:RadGrid>
````



````JavaScript
	        function HierarchyExpanding(sender, eventArgs) {
	            alert("Row: " + eventArgs.get_itemIndexHierarchical() + " is being expanded");
	        }
````



>note get_gridDataItem() is not directly available on the client unless OnRowCreating/OnRowCreated events are hooked up. This is done for optimization purpose. If you need the rowIndex, you can use eventArgs.get_itemIndexHierarchical()
>
