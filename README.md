# Creating custom icons with SVG and animations

1. Create a free [Figma](https://www.figma.com/) account and start a new project.

2. Use the `Pen tool` (find it in the toolbar) to create a check mark (a simple line with 3 points. In technical terms, this is an open path with a stroke and no fill).

3. With the move tool selected, experiment with resizing and changing the shape of your checkmark:
    <!-- TODO: is it called a bounding frame? -->
    - try dragging the `handles` or `sides` of the bounding frame (while dragging, what happens when you hold shift? what happens when you hold alt? how about both?). If you end up with a duplicate shape, you're dragging from the center of the shape. To resize, make sure you grab the handles or the sides.

    - try moving individual points (you may need to double-click a couple of times on your shape for these to appear)

<!-- TODO: is it called a panel? ctrl+f for panel. Toolbar? -->
4. In the `Stroke` panel (right sidebar), change the `color` to `#AAEB8B` and the `width` to `10`. Click the `...` to see advanced stroke options, and give your stroke a `round cap`.

5. In the `Design` panel (right sidebar), click the `broken chain button` (above the `...`) to constrain proportions while resizing. Change the longest dimension of your checkmark (either the `W` or the `H`) to `100`.

6. Looking good! Let's give this file a name. In the center of the toolbar, click where it says `Untitled` and give it the name `Check mark`.

7. In the `Layers` panel (left sidebar) notice the `vector layer` that was created when you used the `Pen tool`. Double click the text to rename it `check-mark`.

8. With your `check-mark` layer is still selected in the `Layers` panel, take a look at the `Export` panel in the right sidebar. Make sure `SVG` is selected, then click the `...` button and check the box labelled `Include "id" Attribute`. Click `Export check-mark` and save your file in the `src` directory in this repo.

9. Open your new svg file in VS Code and try to guess what each part of the code is doing. (The least obvious parts are `viewBox` and `xmlns`. If you're curious you can look them up, but otherwise **just trust that they're important and leave them alone**).

10. Copy the svg element from your source file into the `index.html` file provided. There are many ways to include SVG files in a project. This copy/paste method is known as "inline svg", meaning we can edit the svg code just like regular HTML (e.g. add classes etc.) and apply CSS to it. With "inline svg", we are no longer dependent on the source file, but it's nice to keep for reference (in case something goes wrong) and for reuse in other projects.

## Part 2: Apply styles for different states with CSS pseudo-classes

1. Keep your project open in a browser window and link a new stylesheet to your document.

2. Use any technique you like to place your checkmark in the center of the viewport (horizontally and vertically)

3. Target the `hover` state of the `svg` element. Set its `transform` to `scale(1.5)`.  Experiment: See how it looks if you target the `path` element instead (with the id `check-mark` that we exported earlier). This is because the `svg` element has this `viewBox` attribute which is not scaling. This is why we need to target the `svg` element this time.

4. Add a transition to the `svg` so the scaling happens smoothly in **both directions**, and so it feels like the animation responds quickly to user interaction.
