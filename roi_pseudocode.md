# Interactive Region-of-Interest Drawing Tool

## Objective

Design an interactive tool that allows a user to select
a Region of Interest (ROI) from an image.

## Pseudocode - Revision 2

1. START
2. Initialize the application.
3. Ask the user to select an image.
4. Load the selected image.
5. IF the image cannot be loaded THEN
   - Display "Error: Image not found."
   - Stop the application.
6. ELSE
   - Display the loaded image.
7. Wait for user interaction.
8. Detect mouse button press.
9. Store the starting coordinates.
10. Detect mouse movement.
11. Display a temporary ROI rectangle.
12. Detect mouse button release.
13. Store the final ROI coordinates.
14. Validate the selected ROI.
15. STOP
