## demos/moderngridrowhighlight

Live Link: http://www.claudegauthier.net/demos/ModernGridRowHighlight/

The purpose of this app is to demonstrate how to have rows highlight when they are either added to a store or updated.

This is a modified version of the scaffolding app which is generated by Sencha.

The syntax is as followed:
sencha -sdk ext generate app SomeApp demos/someapp -modern

The code for this app is based from demos/responsivemodern.

I've modified the ListModel so that the store is added using the setStores method.

This allowed me to enhance the scope which the add and update events will use so that I've got access to the view (grid) and the controller.

The app contains a toolbar with a few buttons.

Basically, you can add one record, two records or update the first record.

The entire point of this app isn't where the data comes from, but how to get row highlighting when the store is either added to or records are updated.

You will notice that the add event in the ListModel contains an 'order' config with a value of after.  

This ensures that the view is updated.

I've DRYed the process by creating a highlightRecord method which can take either a single record or an array of records.

The actual animation is set using Ext.Anim.

