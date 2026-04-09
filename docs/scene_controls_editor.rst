Scene Controls and Tools (Editor)
=================================

Tool panel
----------

Within this panel, several buttons are available for creating nodes and relationships. Each button opens a dedicated panel where you can enter all the information needed to define the element you want to create.

Creating semantic shapes
^^^^^^^^^^^^^^^^^^^^^^^^

This panel also includes two buttons that enable the semantic mask drawing mode. To start, click the **Draw a semantic shape** button. From that point, you can place points to enclose the semantic shape; you can create both 2D shapes and polygons. When you're satisfied with the points you've placed, click **Finalize path**, which opens a modal where you can enter:

- A description to assign to the shape
- The stratigraphic node to link it to

After clicking **Done**, the system automatically creates the node associated with the mask and the relationship linking it to the stratigraphic unit.

Scene Controls panel
--------------------

In addition to the brightness control and the list for selecting which relationships to draw -- already available in the viewer -- a set of buttons is provided to:

- Save the graph state
- Manage the objects added from the Shelf to the scene
- Export the graph and the desired semantic shapes

Saving the graph
^^^^^^^^^^^^^^^^

This action is essential to make your changes permanent. When an operation is performed in the editor, it is not written directly to the file on the server. This lets you work on the graph without worrying about damaging the structure as it existed before the current session. To apply the changes to the graph as well, click the **Save changes** button. After using the button, the scene reloads, and you can verify that the changes have been permanently applied.

.. note::
   If you do not save, the next time the page is reloaded, the graph reverts to the state resulting from the last saved modification.

Managing models from the Shelf
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Once 3D models have been added to the scene, you can use two buttons in the panel to:

- **Remove from scene** -- remove the model from the scene
- **Add to graph** -- add it to the graph's nodes

When a model is added to the scene, it is not added as a node in the graph. This way, you can reposition it in the scene and then decide whether to remove it or add it to the graph as a node.

Exporting the graph
^^^^^^^^^^^^^^^^^^^

By clicking **Export scene**, a JSON file describing the scene composition is downloaded. The exported graph reflects the scene as it currently exists, including changes that have not yet been committed on the server. The file is saved to the folder set as the default in your browser settings.

Exporting Semantic Shapes
^^^^^^^^^^^^^^^^^^^^^^^^^

Another feature lets you download the semantic masks present in the visible scene. This allows you to export masks created roughly in the Heriverse editor, import them into a modeling program for refinement, and then recreate the scene with the improved model.

To export the masks, first click **Export Semantic Shapes**. A modal then appears with a selectable list; each item corresponds to a semantic mask present in the scene. After selecting the items of interest, click **Export selected** to start downloading a compressed archive containing the corresponding model files.
