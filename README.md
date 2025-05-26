# Karkhana_assignment

How the Code Is Structured 
The code is organized around a class MobiusStrip with the following structure:

Initialization (init):

Takes radius, width, and points (resolution)

Generates u, v mesh grid

Computes coordinates using parametric equations

get_coordinates():

Implements Möbius parametric equations to compute the 3D surface

plot_strip():

Visualizes the strip in 3D using Matplotlib

calculate_surface_area():

Uses nested loops and cross product of vectors on the mesh to estimate area

calculate_edge_length():

Approximates the length of the boundary by summing distances between edge points

This modular structure makes the code easy to read, debug, and extend.

How Surface Area Was Approximated

The surface is divided into small rectangles (grid cells) on the (u, v) domain

For each cell:

We take 3 corners and form two vectors

Use the cross product of these vectors to estimate a parallelogram area

Add all such small areas to get total surface area

This is a basic form of numerical surface integration

Challenges Faced

The Möbius strip is a non-orientable surface with a twist, so:

Care is needed in grid generation to ensure correct geometry

Avoiding advanced NumPy operations (like gradients and stacking) while keeping accuracy was tricky

Approximation errors may arise due to:

Low resolution (grid too coarse)

Simplified surface estimation

Keeping it easy for beginners while still accurate was the main goal
