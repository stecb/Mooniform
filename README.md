Mooniform
===================

Mooniform is the porting of the famous jquery plugin [uniform](http://uniformjs.com) (by [pixelmatrix](https://github.com/pixelmatrix)) to mootools.

![Screenshot](https://github.com/stecb/mooniform/raw/master/screenshot.png)

How to use
----------

To use it you will simply need to follow the easy instructions below

Basic Example
-------------

First of all you need to include the following html tags:

	#HTML
	<script src="../Source/mooniform.js" type="text/javascript"></script>

	<link href="../Source/css/mooniform.default.css" rel="stylesheet">

Then you can simply use it in this way, for example:

	#JS
	new Mooniform($$('input[type="checkbox"]'));


### Theming:

Theming is done with CSS files and images (see inside /images/ folder).


Class: Mooniform
-----------------

### Syntax

	#JS
	var mooniform_instance = new Mooniform([elements, options]);

### Arguments

1. elements: (*elements*, *array*) The element(s) to attach the mooniform to
2. options: (*object*, optional) The options object

### Options:

All the options of the Mooniform (most of all are about css classes):

- selectClass:        'mooniform-selector',
- radioClass:         'mooniform-radio',
- checkboxClass:      'mooniform-checker',
- fileClass:          'mooniform-uploader',
- filenameClass:      'mooniform-filename',
- fileBtnClass:       'mooniform-action',
- fileDefaultText:    'No file selected',
- fileBtnText:        'Choose File',
- checkedClass:       'mooniform-checked',
- focusClass:         'mooniform-focus',
- disabledClass:      'mooniform-disabled',
- buttonClass:        'mooniform-button',
- activeClass:        'mooniform-active',
- hoverClass:         'mooniform-hover',
- useID:              true,
- idPrefix:           'mooniform',
- resetSelector:      false,
- autoHide:           true

### Public methods:

- update: To update elements after you changed their status by JS (i.e. reset a form)
- lookup: To style new Elements (i.e. loaded with an ajax call)

### Examples

	#JS
  	var elementsToStyle = $$('select, input[type="checkbox"], input[type="radio"], input[type="file"]'),
  	    mooniformInstance = new Mooniform(elementsToStyle);
	
  	//style new elements (loaded by ajax i.e.)
  	  mooniformInstance.lookup(elementsToStyle);
	
  	//if you want to reset a form
      myForm.reset();
      mooniformInstance.update();

License
-------

- [MIT License](http://www.opensource.org/licenses/mit-license.php)
