# GForms (variant)
*** due to function extends for supporting the saved complete google-form page, which can be served via localhost http-server) ***

For installation of http-server, you can use 

```
CMD >> npm install http-server -g
# navigate to the target folder
CMD >> http-server -p 8080 .


CMD >> gh repo clone nx-core/python-gforms-variant
CMD >> cd python-gforms-variant
CMD >> python setup.py install
```

--------------------------------------------

Since my purpose of making this variant is to load any google form (without explicit login), so I just need those contextual items, but not performing the form filling action.

```python3

from gforms import Form
from gforms.elements import Short, Value

# Both way can do ----------
# url = 'https://docs.google.com/forms/d/e/.../viewform'
url = 'http://localhost:8080/form_set_XX/XXXXXXX.htm'

form = Form()

form.load(url)
print(form.to_str(indent=2))  # a text representation, may be useful for CLI applications
```

--------------------------------------------

A python wrapper for public Google Forms.

**This package does not implement form editing / sharing / other actions with user-owned forms**


