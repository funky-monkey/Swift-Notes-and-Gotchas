#Gotchas

####**NSURLErrorDomain 1005:**

[NSURLErrorDomain 1005 Simulator problem](https://stackoverflow.com/questions/25797339/nsurlconnection-get-request-returns-1005-the-network-connection-was-lost)


**Sollution:** Restart the Simulator.


####**Xcode 6.1 Storyboards 0 width and 0 height bug**

**Description:** Most of the time Interface Builder does not show an imageView, table view of other element dragged from the library on the stage/canvas. 

[Width / Height Constrain problem](http://stackoverflow.com/a/26540862)

**Sollution:** Constraints are not optional anymore, always set width and height by entering values and 'add missign constraints'. Don't do this dragging the component and using the mouse. XCode does not like.