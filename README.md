# Milo Wyner's App Portfolio

## [Apance](https://apance.com)

I spent three months doing an internship at Apance, where I got to build various features in SwiftUI for their creative iPad app, which is in early access.

### Layer Editing
This was the most complicated feature to implement. It took a lot of problem solving skills to visualize how a layer could be moved, rotated, and scaled on the screen while also allowing the user to move, rotate, and zoom in/out of the canvas. Especially difficult was getting the correct position when rotating, since you can rotate about any point. I had to convert different trigonometric equations to code functions so the angle and scale could offset the position of the layer on the canvas and the screen.

### Import/Exporting
I implemented a menu to be able to export a PNG or JPG of the project or import a photo from the user’s camera roll or the Files app (including iCloud Drive) to add as a layer to the project. This required converting a UIKit share sheet into a SwiftUI view and sending it an image of the canvas generated from the Metal engine.

### Comments
The last feature I worked on was a commenting interface. The user can drag to highlight an area of focus, then type to enter a comment. Other users can see this as a bubble on the canvas while comments are toggled. Getting these bubbles to remain in the correct position even as the canvas is moved around, rotated and zoomed in/out was a challenge. I solved it by using a stored location of the comment relative to the canvas, then reusing some of the code for the Layer Editing feature to convert the canvas location/scale/rotation to the correct position of the comment bubble. I also used SwiftUI’s animation functionality to make adding these comments fluid.

### Brush Menu and Color Picker
I also worked on some smaller features like a menu of brushes with settings that can be adjusted by custom sliders; and a color picker that allows the user to drag on the screen to select a color on the canvas by sending information about it’s position to the Metal engine and storing the selected color for use when drawing.
