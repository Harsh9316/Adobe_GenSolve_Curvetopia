# Curvetopia

Welcome to **Curvetopia**! This project is dedicated to identifying, regularizing, and beautifying 2D curves. Our mission is to process curves from line art, regularize them, identify symmetry, and complete incomplete curves, ultimately representing them in a set of cubic Bézier curves.

## Project Overview

### Objective

Our primary goal is to convert a set of input polylines into regularized and beautified curves. We aim to handle various types of shapes, from simple lines to complex star shapes. The final output will be a set of curves defined as connected cubic Bézier curves.

### Problem Description

Instead of working with PNG raster images, we start by processing polylines, which are sequences of 2D points. The input consists of finite subsets of paths in \( \mathbb{R}^2 \), and the expected output is a set of regularized, symmetric, and complete paths.

## Sections

### 1. Regularize Curves

In this section, we focus on identifying and regularizing various shapes from the given set of curves. The shapes we target include:

1. **Straight Lines**: Identifying and fitting straight lines.
2. **Circles and Ellipses**: Detecting circles (all points equidistant from a center) and ellipses (two focal points).
3. **Rectangles and Rounded Rectangles**: Identifying rectangles, including those with curved edges.
4. **Regular Polygons**: Detecting polygons with equal sides and angles.
5. **Star Shapes**: Recognizing star shapes with a central point and multiple radial arms.

**Activity**: Test algorithms on hand-drawn shapes and doodles to verify their performance and distinguish between recognizable and non-regularizable shapes.

### 2. Exploring Symmetry in Curves

This section is dedicated to identifying reflection symmetries in closed shapes. Key tasks include:

- **Reflection Symmetries**: Identifying lines of symmetry where the shape can be divided into mirrored halves.
- **Symmetry Fitting**: Transforming points and fitting identical Bézier curves on symmetric points.

**Symmetry Hunt**: Recognize that an identical-looking curve can be represented by different Bézier curves sequences.

### 3. Completing Incomplete Curves

Here, we focus on completing 2D curves that have gaps due to occlusions. The challenge is to naturally complete these curves using:

- **Fully Contained Shapes**: e.g., one circle completely inside another.
- **Partially Contained Shapes**: e.g., a half-circle occluded by another shape.
- **Disconnected Shapes**: e.g., a circle split by a rectangle.

**Guide**: The completion algorithm will consider smoothness, regularity, and symmetry of the shapes.

## Getting Started

### Installation

To get started, clone this repository and install the required dependencies:

```bash
git clone https://github.com/yourusername/curvetopia.git
cd curvetopia

The Identify_Shapes_And_Symmetries notebook gives solutions for regularizing curves and exploring symmetries.
The Occlusion notebooks give solutions for curve completion and handling occlusions. 
Run the notebooks and observe the results.
