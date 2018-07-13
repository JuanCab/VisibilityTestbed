VisibilityTestbed
==================

Demonstrates a problem in Safari with handling visibility of elements in CSS.

To see this rendering bug in action, download the Jupyter notebook and execute
it in the current version of Safari (Version 11.1.2 (13605.3.8)).  

Executing this Jupyter Notebook will generate a simple set of widgets.  The
goal was that selecting from 'yes' or 'no' on the toggle button changes the CSS
for elements on the page, making them visible or invisible.  This works on
Google Chrome, but when run on Safari, it doesn't.  

**Bug Description**  Safari (Version 11.1.2 (13605.3.8)) does **NOT** display
only the proper element after you interact with the toggle button by clicking
on the 'no' and 'yes' repeatedly in the ToggleButtons widget.  The behavior
seems inconsistent. Sometimes both the "yes" and "no" elements are visible,
sometimes the proper element is visible, but offset (indicating that the
`display:none` part of the style has been ignored).

Viewing the HTML/JavaScript/CSS code this Jupiter Notebook generates in
Safari's Developer mode reveals the CSS style (`display: none; visibility:
hidden`) for the hiding the `<DIV>` elements that are supposed to be invisible
does seem to be present, but is being ignored by Safari for unknown reasons.

This bug was initially reported at

https://github.com/JuanCab/AstroInteractives/issues/10

and

https://github.com/jupyter-widgets/ipywidgets/issues/2131

Getting Started
---------------

### Try it online with [Binder](http://mybinder.org/)

[![Binder](https://mybinder.org/badge.svg)](https://mybinder.org/v2/gh/JuanCab/VisibilityTestbed/master?filepath=index.ipynb)

**WARNING**: Once Binder has built the JupyterHub and started your notebook,
when you hit the 'appmode' button, Safari will warn you that you are 'leaving
the page'.  This is normal, just click on 'Leave Page', and this notebook will
execute in the browser and generate the webpage illustrating the bug. 


Goals
-----

- To illustrate the problem so Apple Engineers can solve it. :)

### Dependencies

These Jupyter notebooks require a `jupyter notebook` installation as well as the following python packages:

- `ipywidgets` (version >= 7.2.0)
- `appmode` (This allows the Jupyter notebook to run as an app)

Help / Documentation
--------------------

- Send an email to cabanela@mnstate.edu if you need any help/information.
