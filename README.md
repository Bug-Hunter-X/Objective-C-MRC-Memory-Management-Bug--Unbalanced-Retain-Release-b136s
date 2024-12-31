# Objective-C MRC Memory Management Bug: Unbalanced Retain/Release

This repository demonstrates a subtle bug in Objective-C's manual reference counting (MRC) memory management.  The bug involves an imbalance between `retain` and `release` calls, leading to memory leaks or crashes.  The provided code example showcases the problematic scenario and its solution.

## Bug Description:
The bug lies in an improper handling of object ownership.  An object is retained without a corresponding release, causing a memory leak.  Conversely, releasing an object multiple times or releasing an object that was not retained causes crashes. The subtlety stems from the fact that these issues might not manifest immediately at the point of the coding error.