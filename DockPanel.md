## DockPanel Widget ##

This widget is a retractable panel that can be docked to any one of the screen sides. A custom button will allow the hiding and revealing of the panel.

The button and the panel's content is fully customizable using code or xml markup.

xml markup usage:

```
 <com.MobileAnarchy.Android.Widgets.DockPanel.DockPanel
      android:layout_width="wrap_content"
      android:layout_height="fill_parent"
      android:layout_gravity="right"
      mobileanarchy:dockPosition="right"
      mobileanarchy:handleButtonDrawableId="@drawable/right_dock_handle"
      mobileanarchy:contentLayoutId="@layout/dockpanel_vertical_content"
      mobileanarchy:animationDuration="1000" /> 
```


<a href='http://www.youtube.com/watch?feature=player_embedded&v=NARZmoyZypk' target='_blank'><img src='http://img.youtube.com/vi/NARZmoyZypk/0.jpg' width='425' height=344 /></a>

<a href='http://www.youtube.com/watch?feature=player_embedded&v=ypvSdr_fwfE' target='_blank'><img src='http://img.youtube.com/vi/ypvSdr_fwfE/0.jpg' width='425' height=344 /></a>