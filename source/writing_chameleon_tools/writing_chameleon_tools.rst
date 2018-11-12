
Writing Chameleon Tools
==========================================

A Chameleon tool is a plugin that handles a certain type of task (for example, image classification). Each tool consists of three parts:

a Python class, that plugs in Chameleon to present the UI, and handle handle task data processing, and tool-specific batch processing;
a set of template files (HTMLs) for the tool UI;
a set of static files (javascripts, CSS, etc.) associated with the UI.
When a batch is loaded, the Python class is referenced by name from the batch.json file (see the numerous examples above). The python class extends chameleon.tool.WebTool, implementing the following methods:
