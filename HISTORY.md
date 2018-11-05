# Changelog

#### Version 0.0.2
* View classes now directly importable from the `gsheetz.views` module
* `get_view` function is now bound class method of `SheetViewer` class
	- Use `ClassName.get_view(token,secret,scopes,**kwargs)` to get a view object
	- You can pass keyword arguments to the view constructor using `**kwargs`

#### Version 0.0.1

* Added connection utilities
* Added SheetView and BasicView classes
