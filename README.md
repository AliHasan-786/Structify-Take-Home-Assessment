# Structify-Take-Home-Assessment
## Chord Intersection Counter
## Overview
This program counts the number of intersections formed by chords in a circle. It assumes that all starting and ending points of the chords are unique, and only intersections that happen inside the circle are counted.

## Algorithm
The algorithm works as follows:

Pairs of chords are generated from the input lists of radian values and identifiers.

These chords are then sorted by their starting radian measure.

A balanced binary search tree implemented as a SortedList is used to efficiently manage active chords.

The algorithm iterates over the sorted chords, updating the list of active chords and counting intersections.

Intersections are counted by checking the number of active chords that would intersect with a new chord.

## Running the Code
To run this code, you need Python 3 and the sortedcontainers module installed. You can run the script from the command line as follows:

python count_intersections.py

Make sure you have the radians and identifiers list ready to pass to the count_intersections function.

## Big-O Analysis
The time complexity of the algorithm is O(n log n), where n is the number of chords. This is because:

Sorting the chords takes O(n log n) time.

Each chord insertion and removal operation in the SortedList takes O(log n) time.

The total number of insertions and removals is O(n), leading to O(n log n) for all operations combined.

The space complexity is O(n), as we need to store all chords and the active chords list.

## Edge Cases
The algorithm handles the following edge cases:

Chords that have the same starting or ending radians.

Chords that wrap around the circle past the 0 radian point.
