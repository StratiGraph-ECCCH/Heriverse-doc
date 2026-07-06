XR Reference: Controllers and Commands
=======================================

.. note::

   This is the **operational reference** for the WebXR
   ``immersive-vr`` session. For a friendlier overview of what you
   can do in VR, see :doc:`vr_mode`. This page is meant to be
   scanned when you have a headset on your head and need to remember
   which button does what.

1. Purpose and terminology
--------------------------

This document describes the functions available during a WebXR
``immersive-vr`` session and the commands used to activate them.

- **Right controller**: primary controller used for pointing.
- **Left controller**: secondary controller that hosts the
  wrist-mounted panels.
- **Trigger**: button pressed with the index finger.
- **Grip**: side button pressed by squeezing the controller
  handle.

The physical position and label of each button may vary between
headsets; the roles above are the canonical WebXR mapping.

2. Entering and exiting XR
--------------------------

To enter XR: connect the headset, open a scene, press **VR** in the
top bar and confirm the start of the immersive session. The session
starts in *Node interaction* mode.

To exit: select the red button next to the left-wrist panel with
the right trigger, or use the browser / headset exit control.

3. Quick command reference
--------------------------

.. list-table::
   :header-rows: 1
   :widths: 15 20 30 35

   * - Controller
     - Command
     - Context
     - Result
   * - Right
     - Trigger
     - XR interface
     - Activates the pointed button
   * - Right
     - Trigger
     - Teleport mode
     - Teleports to the aimed point
   * - Right
     - Trigger
     - Node-interaction mode
     - Selects proxies, graph nodes and panel entries
   * - Right
     - Hover / Leave
     - Over a graph node
     - Shows / hides the info panel
   * - Right
     - Grip (hold)
     - Pointing at a stratigraphic node
     - Highlights the associated proxy
   * - Right
     - Grip (release)
     - Highlighted proxy
     - Restores the proxy's previous state
   * - Left
     - Grip near a preview
     - Preview shown
     - Grabs the image or the 3D model
   * - Left
     - Grip (release)
     - Preview being held
     - Positions the preview in the scene
   * - Left
     - Grip
     - Graph open, nothing grabbable nearby
     - Closes the graph
   * - Right
     - **A** / WebXR index 4
     - XR session
     - Moves the user downward
   * - Right
     - **B** / WebXR index 5
     - XR session
     - Moves the user upward

4. Interaction modes
--------------------

Two mode-selector buttons sit on the left wrist. The active mode is
highlighted in green.

Teleport mode
~~~~~~~~~~~~~

Select the button with the pointer icon, aim at a valid surface,
and press the right trigger. In this mode the right trigger does
not open proxies or graph nodes; the interface controls on the
wrist panels remain usable.

Node-interaction mode
~~~~~~~~~~~~~~~~~~~~~

Select the button with the connected-nodes icon. The right trigger
now:

- opens the graph associated with a proxy;
- selects a node inside the graph;
- activates entries on the wrist panels;
- opens the preview of a document node.

5. Left-wrist panels
--------------------

Before a graph is opened, the main panel shows the **temporal
selector**. Use the arrows to scroll through epochs and filters,
and the right trigger to apply the selection.

When a graph is opened, the main panel switches to show the origin
node, its relationships and the neighbouring nodes. The arrows
change which relationship group is displayed.

Selecting an entry with the right trigger displays the node's
details in the **secondary panel** on the wrist. Selecting a node
in this way does **not** open the info panel next to the node in
the scene — that only appears on hover.

6. Graph and semantic nodes
---------------------------

To open a graph:

1. Activate the *Node-interaction* mode.
2. Aim the right controller at a stratigraphic proxy in the scene.
3. Press the right trigger.

While a graph is open, hovering a proxy in the scene no longer
highlights it. To close the graph, press the left grip while no
preview is being held.

When the right pointer enters the area of a graph node, an info
panel appears next to the node. It disappears on Leave. Clicking
instead updates the secondary panel on the right wrist.

In a collaborative session, the graph and the visibility of the
info panel can be synchronised with the other participants.

7. Temporary proxy highlighting
-------------------------------

Use this feature to locate the proxy associated with a
stratigraphic node, even when the proxy is hidden behind other
geometries.

1. Point at a stratigraphic node in the graph with the right
   controller.
2. Press and **hold** the right grip.
3. The associated proxy is highlighted in the scene.
4. Release the grip to restore the previous material and
   visibility.

The command has no effect if the node is not stratigraphic or does
not carry a proxy.

8. Image and 3D previews
------------------------

When a document node is selected, Heriverse loads the first image
or the first compatible 3D model linked to the node. The resource
is resized and shown next to the right controller. This feature is
only available in immersive mode.

Grabbing and placing
~~~~~~~~~~~~~~~~~~~~

1. Move the left controller close to the preview.
2. Press and hold the left grip.
3. Move the controller to reposition the resource.
4. Release the grip at the desired position.

The preview remains in the scene, keeping its position, rotation
and scale. It can be grabbed again by moving the left controller
close and pressing the grip.

The left grip gives priority to grabbing. When no preview is close
enough, the left grip closes the currently open graph instead.

Clearing previews
~~~~~~~~~~~~~~~~~

The preview still attached to the controller is removed when a
non-document node is selected or when the graph is closed. All
placed previews are cleared when the epoch changes and when the XR
session exits.

9. Vertical movement
--------------------

With the standard WebXR mapping:

- the right **A** button (index ``4``) moves the user downward;
- the right **B** button (index ``5``) moves the user upward.

The exact mapping may differ on non-standard controllers.

10. Operational notes
---------------------

- Teleport and node selection are alternative modes of the right
  trigger; switch between them from the left wrist.
- The right grip drives the temporary proxy highlighting.
- The left grip prioritises previews first, then closes the graph.
- Changing epoch clears the graph, the temporary highlights and
  every placed XR preview.
- Resources blocked by CORS rules cannot be shown as previews.

.. seealso::

   :doc:`vr_mode` — narrative introduction to the same feature set,
   with figures showing the wrist panels, teleport pointer and node
   graph.
