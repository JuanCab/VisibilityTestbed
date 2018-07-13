VisibilityTestbed
==================

Demonstrates a problem in Safari with handling visibility of elements in CSS.

To see this rendering bug in action, download the Jupyter notebook and execute
it in the current version of Safari (Version 11.1.2 (13605.3.8)).  

If you don't want to install Jupyter notebooks on your Mac, you can execute it
on the Binder website (see the link below).

This notebook allows you to see the bug in action.  The notebook shows an
attempt to use a Toggle Button to control which text you see. On Google Chrome
it works just as expected, the visible text changes to indicate the appropraite
control panel would have been turned visible.

On Safari (Version 11.1.2 (13605.3.8), the most current release under macOS
11.13.6, it does **NOT**, instead displaying both control panels after you
interact with the toggle button by clicking on the 'no' in the ToggleButtons
widget.

If I go into developer mode on Safari after clicking on 'No', the source code
shows the CSS style for `<DIV>` containing the "Main Sequence Control Panel" is
set to `display: none; visibility: hidden`, yet we see the contents of the
`<DIV>`. As near as I can tell, this is a Safari bug, unless the Jupyter
ntoebook is supposed to somehow tell Safari to refresh its CSS.

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
