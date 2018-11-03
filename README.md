# GSheetz
GSheetz is a small package that I made while trying to connect to the google sheets API. It was really annoying so I made a few classes and functions to make it easier.

The easiest way to use it is through the `gsheetz.views.view.get_view` () function and the `gsheetz.views.view.SheetView` class. This package is really for personal use so I'm not going to spend much time on documentation for now, but if the project expands I'll maybe do stuff to make it legible and stuff like that.

Here's some example usage:

```python
from gsheetz import get_view

TOKEN = 'token.json'
SECRET = 'client_secret.json'
SCOPES = 'https://www.googleapis.com/auth/spreadsheets'
sheetID = '1BxiMVs0XRA5nFMdKvBdBZjgmUUqptlbs74OgvE2upms'
sheetName = 'Class Data'

view = get_view(TOKEN,SECRET,SCOPES)
view.view_sheet(sheetID,sheetName)
```

As you can see, the point of this package is to take care of the boiler-plate for you. If you'd like to interact with the API yourself, simply call `get_view(TOKEN,SECRET,SCOPES).api` to get access to the API object (`service.spreadsheets()`).


### Sources
* [Google Sheets API][sheets-api-homepage] - The docs for the API
* [Guide and Quickstart][API-quickstart] - I literally copy-pasted the python code from this and separated it into multiple functions. I tried figuring out how to use `google.auth` but figured it wasn't worth the extra time to parse through all the docs when the code is already written for me
* [Google Sheets API for Python Developers][sheets-for-py] - the docs that explain how to use the python methods

[shlex]: https://docs.python.org/3/library/shlex.html
[sheets-api-homepage]: https://developers.google.com/sheets/api/
[API-quickstart]: https://developers.google.com/sheets/api/guides/concepts
[sheets-for-py]: https://developers.google.com/api-client-library/python/apis/sheets/v4
