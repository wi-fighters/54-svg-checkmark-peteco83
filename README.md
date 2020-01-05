# Creating custom icons with SVG and animations

## Part 1: Create a custom icon

1. Create a free [Figma](https://www.figma.com/) account and start a new project.

2. Use the `Pen tool` (find it in the toolbar) to create a check mark (a simple line with 3 points. In technical terms, this is an open path with a stroke and no fill).

3. With the move tool selected, experiment with resizing and changing the shape of your checkmark:

    - try dragging the `handles` or `sides` of the bounding box (while dragging, what happens when you hold shift? what happens when you hold alt? how about both?). If you end up with a duplicate shape, you're dragging from the center of the shape. To resize, make sure you grab the handles or the sides.

    - try moving individual points (you may need to double-click a couple of times on your shape for these to appear)

4. In the `Stroke` panel (right sidebar), change the `color` to `#AAEB8B` and the `width` to `10`. Click the `...` to see advanced stroke options, and give your stroke a `round cap`.

5. In the `Design` panel (right sidebar), click the `broken chain button` (above the `...`) to constrain proportions while resizing. Change the longest dimension of your checkmark (either the `W` or the `H`) to `100`.

6. Looking good! Let's give this file a name. In the center of the toolbar, click where it says `Untitled` and give it the name `Check mark`.

7. In the `Layers` panel (left sidebar) notice the `vector layer` that was created when you used the `Pen tool`. Double click the text to rename it `check-mark`.

8. With your `check-mark` layer is still selected in the `Layers` panel, take a look at the `Export` panel in the right sidebar. Make sure `SVG` is selected, then click the `...` button and check the box labelled `Include "id" Attribute`. Click `Export check-mark` and save your file in the `src` directory in this repo.

9. Open your new svg file in VS Code and try to guess what each part of the code is doing. (The least obvious parts are `viewBox` and `xmlns`. If you're curious you can look them up, but otherwise **just trust that they're important and leave them alone**).
