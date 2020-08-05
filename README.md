# lewdo
lewdo : a text-based 3D interface

https://leweyg.github.io/lewdo/index.html

<a href="https://leweyg.github.io/lewdo/index.html">![lewdo](lewdo/lewdo.png)</a>

## Introduction
'lewdo' is a text-based 3D windowing and application environment. Both the output display and input system are modelled as simply 3d buffers of text with update events (see `string3`). Much as UNIX processes have 'standard in' and 'standard out' file streams associated with each, lewdo applications simply use a 3d buffer (with frame update events) to model both the standard input and standard output streams of the application. Sub-processes can then be created to host inner content, such as buttons or labels, and user interfaces can be naturally built out there-by. Currently it is hosted within an HTML page as pure CSS; WebGL/XR and Unity versions are in the works.

### Background

Designing a 3D interface is a complex problem; 'lewdo' attempts to tackle a subset of these design problems within the somewhat artificial context of a purely 'text-based 3d interface'. It contains numerous apps, and data models to explore interaction within that environment.

Also yes, the author ( <a href="http://www.lewcid.com/lg/aboutme.html">Lewey Geselowitz</a> ), is aware that non-text-based 3D interfaces work (he generally works on on AR/MR/VR and even <a href="http://www.4dprocess.com/4d/index.html">4D interfaces</a>, within which this sort of interface may be interesting). But really this is just a test, and reminds him of the old-days; while also providing space to really explore 3D interaction in a pure form.

## Example App

    function helloWorld(app) {
        app.app_out.copy(string3("Hello\v\nWorld"));
        app.app_out.frameStep();
    }
    lewdo_app_prototype.all_apps.apps["helloWorld"] = helloWorld;

This application outputs a 3D "Hello World" to the display, with "Hello" at the closest depth, and "World" below that. `string3` treats the `\n` as `New Line`, but the `\v` is interpreted as `New Page`. The call to `frameStep()` informs any subscribers that the frame is now ready to be recieved (common in graphics architectures). Also the line at the bottom add this method to the standard list of apps.

## Example App with Input

For an example app which reads it's input and repeats it back volumetrically, see [repeatMe.js](lewdo/examples/repeatMe.js)

## lewdo_app()

This methods create a new app instance with the following default properties. Most "applications" are actually methods that take an app instance as input, and interact via subscriptions to it's input and output buffers.

| Property | Type | Description |
| ----- | ----- |
| app_out | string3 | Output/display buffer |

## string3()


