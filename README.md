# STLtoOpenFOAM

This repository contains a Python script for analyzing STL geometry files using VTK. The script computes various geometric properties such as volume, surface area, curvature, and more. It also identifies points inside and outside the geometry and generates a blockMeshDict for OpenFOAM.

## Author

Amr Emad

## Dependencies

- VTK (Visualization Toolkit)
- NumPy

## Installation

You can install the required dependencies using pip:

```sh
pip install vtk numpy

Usage
Run the script from the command line as follows:
python stlAnalysis.py examples/flange.stl --volume --surface_area --center_of_mass --bounding_box --curvature --surface_normals --facet_areas --edge_lengths --aspect_ratios --inside_outside_points --generate_blockMeshDict --buffer 10 --max_buffer 20
Options
--volume: Compute volume
--surface_area: Compute surface area
--center_of_mass: Compute center of mass
--bounding_box: Compute bounding box
--curvature: Compute curvature
--surface_normals: Compute surface normals
--facet_areas: Compute facet areas
--edge_lengths: Compute edge lengths
--aspect_ratios: Compute aspect ratios
--inside_outside_points: Compute inside and outside points
--generate_blockMeshDict: Generate blockMeshDict for OpenFOAM
--buffer <value>: Buffer size to add around the bounding box (default: 10)
--max_buffer <value>: Maximum buffer size allowed for the bounding box (default: 20)

Features
Volume Calculation
Calculate the volume of the STL geometry.

Surface Area Calculation
Calculate the surface area of the STL geometry.

Center of Mass Calculation
Compute the center of mass of the STL geometry.

Bounding Box Calculation
Determine the minimum and maximum bounds of the STL geometry.

Curvature Calculation
Calculate the curvature of the STL geometry. Supports mean, Gaussian, maximum, and minimum curvatures.

Surface Normals Calculation
Compute the surface normals and count the number of outward-facing and inward-facing normals.

Facet Areas Calculation
Determine the minimum and maximum facet areas in the STL geometry.

Edge Lengths Calculation
Calculate the minimum and maximum edge lengths in the STL geometry.

Aspect Ratios Calculation
Compute the minimum and maximum aspect ratios of the facets in the STL geometry.

Inside and Outside Points Calculation
Identify points inside and outside the STL geometry.

Generate blockMeshDict
Generate a blockMeshDict file for OpenFOAM based on the STL geometry.

Example Directory Structure
STLtoOpenFOAM/
├── .gitignore
├── LICENSE
├── README.md
├── stlAnalysis.py
└── examples/
    └── example.stl
	
Script Documentation

"""
-------------------------------------------------------------------------------
    VTK is free software: you can redistribute it and/or modify it
    under the terms of the GNU Lesser General Public License as published by
    the Free Software Foundation, either version 2.1 of the License, or
    (at your option) any later version.

    VTK is distributed in the hope that it will be useful, but WITHOUT
    ANY WARRANTY; without even the implied warranty of MERCHANTABILITY or
    FITNESS FOR A PARTICULAR PURPOSE.  See the GNU Lesser General Public License
    for more details.

    You should have received a copy of the GNU Lesser General Public License
    along with VTK.  If not, see <http://www.gnu.org/licenses/>.

Application
    stlAnalysis

Group
    grpGeometryAnalysis

Description
    Script to analyze STL geometry files using VTK. This script computes
    various geometric properties such as volume, surface area, curvature,
    and more. It also identifies points inside and outside the geometry
    and generates a blockMeshDict for OpenFOAM.
    
Author    
    Amr Emad
Date
    June 21, 2024
Version
    v1.2

Dependencies
    - VTK (pip install vtk)
    - NumPy (pip install numpy)
    - JSON (Standard library)

Usage
    Run the script from the command line as follows:

    python stlAnalysis.py <path_to_stl_file> [options]

    Example:
    python stlAnalysis.py D:/AmrEmadDev/dev/flange.stl --volume --surface_area --center_of_mass --bounding_box --curvature --surface_normals --facet_areas --edge_lengths --aspect_ratios --inside_outside_points --generate_blockMeshDict --buffer 10 --max_buffer 20

    Options:
    --volume: Compute volume
    --surface_area: Compute surface area
    --center_of_mass: Compute center of mass
    --bounding_box: Compute bounding box
    --curvature: Compute curvature
    --surface_normals: Compute surface normals
    --facet_areas: Compute facet areas
    --edge_lengths: Compute edge lengths
    --aspect_ratios: Compute aspect ratios
    --inside_outside_points: Compute inside and outside points
    --generate_blockMeshDict: Generate blockMeshDict for OpenFOAM
-------------------------------------------------------------------------------
"""

License
This project is licensed under the terms of the GNU Lesser General Public License (LGPL).


This `README.md` file provides comprehensive documentation for your `STLtoOpenFOAM` repository, including installation instructions, usage examples, options, features, and detailed script documentation. You can copy this content and save it as `README.md` in your repository.
