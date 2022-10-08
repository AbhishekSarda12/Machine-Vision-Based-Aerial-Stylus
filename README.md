# Machine-Vision-Based-Aerial-Stylus
Python Stylus
python-stylus bridges your Python code and the Stylus library.

Prerequisites
This libraries assumes you have a couple of things in place already for stylus to work:

Node installed with the node command available to use in your runtime.
Stylus installed in your working directory's node_modules folder or in a location specified in your NODE_PATH environment variable.
Installation
pip install stylus

Usage
from stylus import Stylus
compiler = Stylus()

compiler.compile("""
border-radius()
  -webkit-border-radius arguments
  -moz-border-radius arguments
  border-radius arguments


body
  font 12px Helvetica, Arial, sans-serif

a.button
  border-radius 5px
""")

# import plugins
compiler.use("nib")

compiler.compile("""
@import 'nib'
body
  background: linear-gradient(top, white, black)
""")
