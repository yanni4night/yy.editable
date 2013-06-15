#yy.editable


***yy.editable*** is a quite simple jQuery plugin that can make text editable .The editable element can be any HTML elements that have *innerHTML*,for examples,*div*,*p*,*span*,etc,but not *input*,*img* or *textarea*.

##install

if you're using [requirejs](http://requirejs.org),you need configure deps in require.config:

    'jquery.yy.editable':{deps:['jquery']}

or else you'll get a no method found error.

If you use it directly in HTML,

    <script type="text/javascript"  src="jquery.yy.editable.min.js"></script>

after jquery.js.

##usage

    $('.editable').yeditable({});

The parameter includes:

**inputAutoSize**: *true/false*  =>whether the input should be resize as the origin text.

**inputAutoClass**: *true/false* =Whether the input should have the same class as the origin text.

**styleClass**: *'className'*=>If inputAutoClass is set to false,these one or more classes will be added to input.

**inputText**: *'input'/'textarea'* =>The input can act as a input with type=text,or a textarea.Note that Line break will act as a white space.

**validate**: *function(newValue,oldValue){}* =>Validate the new value,false means wrong value and the text is still editable.

**onEditSucceed**:*function(oldValue ,newValue){}* =>invoke when validate pass

**onEditFailed**:*function(oldValue ,newValue){}* =>invoke when validate failed

**onBeforeEdit**: *function(){oldValue}* =>Before the edit.Return false means this text cannot be editable.

**onAfterEdit**: *function(){oldValue, newValue}* =>After edited successfully.If sync is set true,this will only be invoke sync successfully.
