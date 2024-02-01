# Structify-Take-Home-Assessment

## Overview
This Python program calculates the number of intersections that occur inside a circle formed by various chords. It is assumed that each chord has unique starting and ending points.

## Algorithm
The algorithm operates by following these steps:

- It generates pairs of chords using input lists of radian values and identifiers.
- These chords are sorted based on their starting radian values.
- A balanced binary search tree, implemented as a SortedList, efficiently manages active chords.
- As the algorithm iterates over the sorted chords, it updates the list of active chords and counts the intersections.
- Intersections are identified by counting the number of active chords that intersect with each new chord.

## Running the Code
Ensure Python 3 and the sortedcontainers module are installed. Run the script from the command line with:

python count_intersections.py

Prepare the radians and identifiers list to pass to the count_intersections function before running.

## Big-O Analysis
The time complexity of the algorithm is O(n log n), with n being the number of chords, because:

## Sorting the chords requires O(n log n) time.
- Each operation for chord insertion or removal in the SortedList takes O(log n) time.
- With O(n) total insertions and removals, the combined operations also result in O(n log n) complexity.
- The space complexity is O(n), needed for storing all chords and the active chords list.

## Edge Cases
The algorithm has been tested against edge cases, including:

Chords sharing the same starting or ending radians.
Chords that wrap around the circle, crossing the 0 radian mark.
These cases are handled appropriately within the algorithm to ensure accurate intersection counts.

## Running the Tests
Unit tests are included to verify the algorithm against various scenarios:

python -m unittest test_count_intersections.py

The test suite covers:

- Single intersection scenarios.
- No intersection scenarios.
- Multiple intersection scenarios.
- Chords with identical start or end points.
- Chords that wrap around the 0 radian point to ensure the algorithm's robustness.
