## ThreasholdEditText Widget ##

A new OnThresholdTextChanged event was added to the view that will be fired after a specific (configurable) delay from the last received input on that EditText view.

This lets you start a long running process (like a search process) after the user has finished entering some input in the EditText view without the need to add another "Submit" button and handle its "Clicked" event.

If you have your own custom view that extends the "standard" EditText, and you want this additional functionality, all you need to do is to update your class and extend the ThresholdEditText instead of the "standard" EditBox.

<a href='http://www.youtube.com/watch?feature=player_embedded&v=udIRwgBIi4Q' target='_blank'><img src='http://img.youtube.com/vi/udIRwgBIi4Q/0.jpg' width='425' height=344 /></a>

and another ScreenCast - Stocks search:

<a href='http://www.youtube.com/watch?feature=player_embedded&v=H9cYe6PVPHI' target='_blank'><img src='http://img.youtube.com/vi/H9cYe6PVPHI/0.jpg' width='425' height=344 /></a>