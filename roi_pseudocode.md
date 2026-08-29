# Interactive Region-of-Interest Drawing Tool

## Objective

Design an interactive tool that allows a user to load an image,
draw an ROI, extract the selected region, and optionally save it.

## Input

Image selected by the user.

## Output

Selected ROI coordinates and cropped ROI image.

## Pseudocode - Revision 3

1. START

2. Initialize the application.

3. Ask the user to select an image.

4. Load the selected image.

5. IF the image cannot be loaded THEN
      Display "Error: Image not found or invalid."
      Stop the application.
   ELSE
      Display the loaded image.
   END IF

6. Create an empty ROI selection area.

7. Wait for the user to interact with the image.

8. IF the user presses the mouse button THEN
      Store the starting point (X1, Y1).
      Set ROI drawing mode to ACTIVE.
   END IF

9. IF the user moves the mouse while ROI drawing mode is ACTIVE THEN
      Store the current point (X2, Y2).
      Display a temporary ROI rectangle.
   END IF

10. IF the user releases the mouse button THEN
       Set ROI drawing mode to INACTIVE.
       Store the final ROI coordinates.
    END IF

11. Validate the selected ROI.

12. IF the ROI has zero width or zero height THEN
       Display "Invalid ROI. Please select again."
       Return to Step 7.
    END IF

13. Extract the selected region from the original image.

14. Display the cropped ROI separately.

15. Ask the user whether the ROI should be saved.

16. IF the user selects SAVE THEN
       Save the cropped ROI.
       Display "ROI saved successfully."
    ELSE
       Continue without saving.
    END IF

17. Ask the user whether another ROI should be selected.

18. IF the user selects YES THEN
       Clear the previous ROI.
       Return to Step 7.
    ELSE
       Continue.
    END IF

19. Close the image window.

20. Release all resources.

21. STOP

## Workflow

START
  ↓
Load Image
  ↓
Display Image
  ↓
User Draws ROI
  ↓
Capture Coordinates
  ↓
Validate ROI
  ↓
Extract ROI
  ↓
Display Cropped ROI
  ↓
Save ROI?
  ↓
Another ROI?
  ↓
Close Application
  ↓
STOP
