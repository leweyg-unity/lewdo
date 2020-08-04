# lewdo
lewdo : a text-based 3D interface

https://leweyg.github.io/lewdo/index.html

<a href="https://leweyg.github.io/lewdo/index.html">![lewdo](lewdo/lewdo.png)</a>

## Introduction
'lewdo' is a text-based 3D windowing and application environment. Both the output display and input model are simply 3d buffers of text ('string3'). Much as UNIX processes have 'standard in' and 'standard out' file streams associated with each, lewdo applications simply use a 3d buffer (with frame update events) to model both the standard input and standard output streams of the application. Sub-processes can then be created to host inner content, such as buttons or labels, and user interfaces can be naturally built out there-by. Currently it is hosted within an HTML page as pure CSS; WebGL/XR and Unity versions are in the works.

### Background

Designing a 3D interface is a complex problem; 'lewdo' attempts to tackle a subset of these design problems within the somewhat artificial context of a purely 'text-based 3d interface'. It contains numerous apps, and data models to explore interaction within that environment.

Also yes, the author ( <a href="http://www.lewcid.com/lg/aboutme.html">Lewey Geselowitz</a> ), is aware that non-text-based 3D interfaces work (he generally works on on AR/MR/VR and even <a href="http://www.4dprocess.com/4d/index.html">4D interfaces</a>, within which this sort of interface may be interesting). But really this is just a test, and reminds him of the old-days; while also providing space to really explore 3D interaction in a pure form.

## Example App

## Example App with Input

## lewdo_app()

## string3()


