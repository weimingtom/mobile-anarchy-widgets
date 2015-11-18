## Drag&Drop Infrastructure ##

This infrastructure can transform any view on the screen to a "DropZone" that listen to OnDragEnter, OnDragLeft and OnDropped events.

First, you must add the "DragSurface" view to your topmost view hierarchy:
```
<com.MobileAnarchy.Android.Widgets.DragAndDrop.DragSurface
  android:id="@+id/dragsurface" android:layout_height="fill_parent"
  android:layout_width="fill_parent" />
```

Next, initialize the DragAndDropManager class, by providing a DragSurface instance:
```
DragSurface dragSurface = (DragSurface)findViewById(R.id.dragsurface);
DragAndDropManager.getInstance().init(dragSurface);
```

Now we are ready to add some DropZones:
```
DropZone dropzone1 = new DropZone(findViewById(R.id.FrameLayoutDropZone1), dropzoneListener);
DragAndDropManager.getInstance().addDropZone(dropzone1);

DropZone dropzone2 = new DropZone(findViewById(R.id.FrameLayoutDropZone2), dropzoneListener);
DragAndDropManager.getInstance().addDropZone(dropzone2);
```

That's it. all we need to do now, is to start a drag session when the user touch the screen:
```

private OnTouchListener onTouchListener = new OnTouchListener() {
		
	@Override
	public boolean onTouch(View v, MotionEvent event) {
		if (event.getAction() == MotionEvent.ACTION_DOWN)
		{
			DraggableItem draggedItem = new DraggableItem(v, DraggableViewsFactory.getLabel("Drop Me"));

			// Start dragging
			DragAndDropManager.getInstance().startDragging(this, draggedItem);
				
			return true;
		}
		return false;
	}
};
```


<a href='http://www.youtube.com/watch?feature=player_embedded&v=hDfDpf6uHi0' target='_blank'><img src='http://img.youtube.com/vi/hDfDpf6uHi0/0.jpg' width='425' height=344 /></a>